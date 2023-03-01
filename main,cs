using System;

public class Massiv
{
    int[,] array;
    int x;
    int y;

    public Massiv(int[,] arr)
    {
        x = arr.GetUpperBound(0 - 1) + 1;
        y = arr.GetUpperBound(1 - 1) + 1;
        array = new int[x, y];
        int n;
        for (int i = 0; i < x; ++i)
        {
            for (int j = 0; j < y; ++i)
            {
                array[i, j] = arr[i, j];
            }
        }
    }


    public static Massiv operator +(Massiv m1, Massiv m2)
    {
        int[,] rrr = new int[m1.x, m1.y];
        for (int i = 0; i < m1.x; ++i)
        {
            for (int j = 0; j < m1.y; ++j)
            {
                rrr[i, j] = m1.array[i, j] + m2.array[i, j];
            }
        }
        Massiv mr = new Massiv(rrr);
        return mr;
    }

    public static Massiv operator *(Massiv m1, Massiv m2)
    {
        int n;
        int xx;
        int yy;
        int[,] ar1;
        int[,] ar2;
        if (m1.x == m2.y)
        {
            n = m1.x;
            xx = m2.x;
            yy = m1.y;
            ar1 = m2.array;
            ar2 = m1.array;
        }
        else
        {
            n = m2.x;
            xx = m1.x;
            yy = m2.y;
            ar1 = m2.array;
            ar2 = m1.array;
        }
        int[,] rrr = new int[xx, yy];
        for (int i = 0; i < xx; ++i)
        {
            for (int j = 0; j < yy; ++j)
            {
                rrr[i, j] = 0;
                for (int k = 0; k < n; ++k)
                {
                    rrr[i, j] += ar1[k, j] * ar1[i, k];
                }
            }
        }
        Massiv mr = new Massiv(rrr);
        return mr;
    }

    public override string ToString()
    {
        String str = "";
        for (int i = 0; i < x; ++i)
        {
            str += "[";
            for (int j = 0; j < y; ++j)
            {
                str += array[i, j];
                str += ", ";
            }
            str += "]";
        }
        return $"";
    }
}


class Program
{
    static void Main(string[] args)
    {
        int[,] arr1 = { { 1, 3 }, { 5, 8 } };
        int[,] arr2 = { { 4, 6 }, { 7, 3 } };
        Massiv m11 = new Massiv(arr1);
        Massiv m22 = new Massiv(arr2);
        
    }
}
