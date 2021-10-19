# Triangle_Plane

There are N Points in 2d Cartesian Plane You Have To Calculate The Area Of largest Triangle In The Cartesian Plane and also calculate the largest perimeter of triangle formed in the plane

Cartesian Plane is Given in form of 2d arrray with n  rows and 2 column where first column is for x coordinate and second row is for y coordinate.

## Input Output format

**Input :**

Take input for n rows and in each row take input for x and y coordinate.

**Output :**

First line of output contains the largest area and second line contains largest perimeter.

**Constraints :**

    N>=3 and N<=100
    Coordinate values can also have negative values because we are considering cartesian plane
</br>

**Testcase 1:**

    Input  : points = [[0,0],[0,1],[1,0],[0,2],[2,0]]
    Output : Area:2.00 and Perimter:4+2*(underroot 2)
    
Approach Simply Use Herons Formula to find the Area & Perimeter 

Area of triangle ABC = √s(s-a)(s-b)(s-c), where s = Perimeter/2 = (a + b + c)/2

We will use 3 nested loop since we want to find the max area we will consider all possible combinations

Time Complexity ->O(N^3)
Space Complexity -> O(1)

```
class Solution {
public:
    pair<double,double> largestTriangleArea(vector<vector<int>>& points) {
    int n=points.size();
    double maxArea=0;
    double perimeter = 0;
         double d1,d2,d3,area,s;
    for(int i=0;i<n;i++)
    {
        for(int j=i+1;j<n;j++)
        {
            for(int k=j+1;k<n;k++)
            {
                    d1=sqrt((double)pow(points[i][0]-points[j][0],2)+pow(points[i][1]-points[j][1],2));    
                    d2=sqrt((double)pow(points[j][0]-points[k][0],2)+pow(points[j][1]-points[k][1],2));
                    d3=sqrt((double)pow(points[i][0]-points[k][0],2)+pow(points[i][1]-points[k][1],2));
                    s=(d1+d2+d3)/2.00000;
                    area=(double)sqrt(s*(s-d1)*(s-d2)*(s-d3));
                     perimeter = max(perimeter,d1+d2+d3);
                        if(maxArea<area)
                        maxArea=area;   
            }
        }
    }
    pair<double,double> answer;
    answer.first = area;
    answer.second = perimeter;
    return answer;
}
};
