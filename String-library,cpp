#include <iostream>
using namespace std;

class STRING
{
    char *array = new char[50];

public:
    STRING(char a[])
    {
        for (int i = 0; i < sizeofarray(a); i++)
        {
            array[i] = a[i];
        }
        array[sizeofarray(a)] = '\0';
    }
    STRING()
    {
    }
    STRING(int size)
    {
    }
    STRING operator+(STRING &b)
    {
        STRING temp;
        for (int i = 0; i < this->sizeofarray(this->array); i++)
        {
            temp.array[i] = this->array[i];
        }
        for (int i = 0; i < b.sizeofarray(b.array); i++)
        {
            temp.array[sizeofarray(array) + i] = b.array[i];
        }
        temp.array[this->sizeofarray(this->array) + b.sizeofarray(b.array)] = '\0';
        return temp;
    }
    void operator+=(STRING &b)
    {
        int size = this->sizeofarray(this->array);
        for (int i = 0; i < b.sizeofarray(b.array); i++)
        {
            this->array[size + i] = b.array[i];
        }
        this->array[size + b.sizeofarray(b.array)] = '\0';
    }
    char &operator[](int num)
    {
        return array[num];
    }
    bool operator==(STRING &b)
    {
        int count = 0;
        if (this->sizeofarray(array) != b.sizeofarray(b.array))
        {
            return false;
        }
        else
        {
            for (int i = 0; i < this->sizeofarray(array); i++)
            {
                if (array[i] == b.array[i])
                {
                    count++;
                }
            }
            if (count == this->sizeofarray(array))
            {
                return true;
            }
            else
            {
                return false;
            }
        }
    }
    bool operator!=(STRING &b)
    {
        int count = 0;
        if (this->sizeofarray(array) != b.sizeofarray(b.array))
        {
            return true;
        }
        else
        {
            for (int i = 0; i < this->sizeofarray(array); i++)
            {
                if (array[i] == b.array[i])
                {
                    count++;
                }
            }
            if (count == this->sizeofarray(array))
            {
                return false;
            }
            else
            {
                return true;
            }
        }
    }
    bool operator>(STRING &b)
    {

        bool t = *this == b;
        if (t == 1)
        {
            return 0;
        }
        else
        {
            for (int i = 0; i < this->sizeofarray(this->array); i++)
            {
                if (this->array[i] > b.array[i])
                {
                    return 1;
                }
                else if (this->array[i] < b.array[i])
                {
                    return 0;
                }
                else if (this->array[i] == b.array[i])
                {
                    continue;
                }
            }
        }
    }
    bool operator<(STRING &b)
    {
        bool t = *this == b;
        if (t == 1)
        {
            return 0;
        }
        else
        {
            for (int i = 0; i < this->sizeofarray(this->array); i++)
            {
                if (this->array[i] < b.array[i])
                {
                    return 1;
                }
                else if (this->array[i] > b.array[i])
                {
                    return 0;
                }
                else if (this->array[i] == b.array[i])
                {
                    continue;
                }
            }
        }
    }
    STRING operator()(int num1, int num2)
    {
        int count = 0;
        STRING temp;
        for (int i = num1; i <= num2; i++)
        {
            temp.array[count++] = this->array[i];
        }
        temp.array[count] = '\0';
        return temp;
    }
    STRING &operator=(STRING b)
    {
        for (int i = 0; i < b.size(); i++)
        {
            this->array[i] = b.array[i];
        }
        this->array[b.size()] = '\0';
        return (*this);
    }
    STRING operator<<(int num)
    {
        STRING temp;
        for (int i = 0; i < num; i++)
        {
            temp.array[i] = this->array[i];
        }
        temp.array[num] = '\0';
        for (int i = 0; i < this->sizeofarray(this->array) - num; i++)
        {
            this->array[i] = this->array[num + i];
        }
        this->array[(sizeofarray(this->array)) - num] = '\0';
        return temp;
    }
    STRING operator>>(int num)
    {
        STRING temp;
        int count = 0;
        for (int i = this->sizeofarray(this->array) - num; i < this->sizeofarray(this->array); i++)
        {
            temp.array[count] = this->array[(this->sizeofarray(this->array)) - count - 1];
            count++;
        }
        temp.array[count] = '\0';
        for (int i = 0; i < this->sizeofarray(this->array) - num; i++)
        {
            this->array[i] = this->array[i];
        }
        this->array[this->sizeofarray(this->array) - num] = '\0';
        return temp;
    }
    int sizeofstring(string str)
    {
        int count = 0;
        for (int i = 0; str[i] != '\0'; i++)
        {
            count++;
        }
        return count;
    }
    int sizeofarray(char a[])
    {
        int count = 0;
        for (int i = 0; a[i] != '\0'; i++)
        {
            count++;
        }
        return count;
    }
    int size()
    {
        return this->sizeofarray(this->array);
    }
    ~STRING()
    {
    }
    friend ostream &operator<<(ostream &a, STRING &b);
    friend istream &operator>>(istream &input, STRING &b);
};
ostream &operator<<(ostream &output, STRING &b)
{
    for (int i = 0; i < b.sizeofarray(b.array); i++)
    {
        output << b.array[i];
    }
    return output;
}
istream &operator>>(istream &input, STRING &b)
{
    input >> b.array;
    return input;
}

int main()
{
    int ch;
    char st;
    bool t;
    STRING a("ABCDEFG");
    STRING b("1234567");

    cout << "\nGIVEN Two strings:\na: ABCDEFG\nb: 1234567";
    cout << "\nWhich Function you want to use? Enter:\n1)String concatenation\n2)String concatenation(Adding in itself)\n3)Get individual characters\n4)Set individual characters\n5)Test string equality\n6)Test string inequality\n7)String comparison(>)\n8)String comparison(<)\n9)Get sub-string\n10)Print string\n11)Input string\n12)String assignment\n13)String left shift\n14)String right shift\n";
    cin >> ch;
    if (ch == 1)
    {
        cout << "\na: " << a << "\nb: " << b;
        STRING c;
        cout << "\nWhat you want?\n1) c = a + b or 2) c = b + a \nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            c = a + b;
        }
        else if (ch == 2)
        {
            c = b + a;
        }
        else
        {
            cout << "\nInvalid Input";
        }

        cout << endl
             << "c: " << c;
    }
    else if (ch == 2)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nWhich one?\n1)a+=b or 2)b+=a\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            a += b;
            cout << "\na: " << a;
        }
        else if (ch == 2)
        {
            b += a;
            cout << "\nb: " << b;
        }
        else
        {
            cout << "\nInvalid Input";
        }
    }
    else if (ch == 3)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << endl
             << "Enter Index:\n";
        cin >> ch;
        cout << "In which string: Enter a or b: ";
        cin >> st;
        if (st == 'a')
        {
            if (ch < a.size() && ch >= 0)
            {
                char d = a[ch];
                cout << "\nOutput: "
                     << d;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else if (st == 'b')
        {
            if (ch < b.size() && ch >= 0)
            {
                char d = b[ch];
                cout << "\nOutput: "
                     << d;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else
        {
            cout << "\nInvalid Input";
        }
    }
    else if (ch == 4)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << endl
             << "Enter Index:\n";
        cin >> ch;
        cout << "In which string: Enter a or b: ";
        cin >> st;
        if (st == 'a')
        {
            if (ch < a.size() && ch >= 0)
            {
                cout << "\nEnter Value: ";
                cin >> st;
                a[ch] = st;
                cout << endl
                     << "Output: "
                     << a;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else if (st == 'b')
        {
            if (ch < b.size() && ch >= 0)
            {
                cout << "\nEnter Value: ";
                cin >> st;
                b[ch] = st;
                cout << endl
                     << "Output: "
                     << b;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else
        {
            cout << "\nInvalid Input";
        }
    }
    else if (ch == 5)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nYou want to compare:\n1)a with a\n2)a with b\n3)b with b\nEnter(1,2 or 3): ";
        cin >> ch;
        if (ch == 1)
        {
            t = a == a;
            if (t == 1)
            {
                cout << "\nTrue!Both are equal";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are unequal";
            }
        }
        else if (ch == 2)
        {
            t = a == b;
            if (t == 1)
            {
                cout << "\nTrue!Both are equal";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are unequal";
            }
        }
        else if (ch == 3)
        {
            t = b == b;
            if (t == 1)
            {
                cout << "\nTrue!Both are equal";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are unequal";
            }
        }
    }
    else if (ch == 6)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nYou want to compare:\n1)a with a\n2)a with b\n3)b with b\nEnter(1,2 or 3): ";
        cin >> ch;
        if (ch == 1)
        {
            t = a != a;
            if (t == 1)
            {
                cout << "\nTrue!Both are unequal";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are equal";
            }
        }
        else if (ch == 2)
        {
            t = a != b;
            if (t == 1)
            {
                cout << "\nTrue!Both are unequal";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are equal";
            }
        }
        else if (ch == 3)
        {
            t = b != b;
            if (t == 1)
            {
                cout << "\nTrue!Both are equnual";
            }
            else if (t == 0)
            {
                cout << "\nFalse!Both are equal";
            }
        }
    }
    else if (ch == 7)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nYou want to check:\n1) a > b or 2) b > a\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            t = a > b;
            if (t == 1)
            {
                cout << "\nTrue!";
            }
            else
            {
                cout << "\nFalse!";
            }
        }
        else if (ch == 2)
        {
            t = b > a;
            if (t == 1)
            {
                cout << "\nTrue!";
            }
            else
            {
                cout << "\nFalse!";
            }
        }
        else
        {
            cout << "\nInvalid Input";
        }
    }
    else if (ch == 8)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nYou want to check:\n1) a < b or 2) b < a\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            t = a < b;
            if (t == 1)
            {
                cout << "\nTrue!";
            }
            else
            {
                cout << "\nFalse!";
            }
        }
        else if (ch == 2)
        {
            t = b < a;
            if (t == 1)
            {
                cout << "\nTrue!";
            }
            else
            {
                cout << "\nFalse!";
            }
        }
        else
        {
            cout << "\nInvalid Input";
        }
    }
    else if (ch == 9)
    {
        STRING c;
        int ind1, ind2;
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nEnter Starting Index: ";
        cin >> ind1;
        cout << "\nEnter Ending Index: ";
        cin >> ind2;
        cout << "In which string: Enter a or b: ";
        cin >> st;
        if (st == 'a')
        {
            if (ind1 >= 0 && ind2 < a.size())
            {
                c = a(ind1, ind2);
                cout << endl
                     << "Output: "
                     << c;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else if (st == 'b')
        {
            if (ind1 >= 0 && ind2 < b.size())
            {
                c = b(ind1, ind2);
                cout << endl
                     << "Output: "
                     << c;
            }
            else
            {
                cout << "\nInvalid Index";
            }
        }
        else
        {
            cout << "\nWrong Input";
        }
    }
    else if (ch == 10)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nWhich String?\n1)a or 2)b:\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            cout << "\na: " << a;
        }
        else if (ch == 2)
        {
            cout << "\nb: " << b;
        }
    }
    else if (ch == 11)
    {
        STRING c;
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nEnter String:";
        cin >> c;
        cout << "\nc: " << c;
    }
    else if (ch == 12)
    {
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nWhat you want to do?\n1) a = b or 2) b = a\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            a = b;
            cout << endl
                 << "a: " << a;
        }
        else if (ch == 2)
        {
            b = a;
            cout << endl
                 << "b: " << b;
        }
        else
        {
            cout << "Wrong Input!";
        }
    }
    else if (ch == 13)
    {
        int num;
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nEnter How much you want to left shift?: ";
        cin >> num;
        cout << "\nWhich String?\n1)a or 2)b\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            if (num < a.size())
            {
                STRING c;
                c = a << num;
                cout << "\na: " << a;
                cout << "\nc: " << c;
            }
            else
            {
                cout << "\nCannot do this much left shift!";
            }
        }
        else if (ch == 2)
        {
            if (num < b.size())
            {
                STRING c;
                c = b << num;
                cout << "\nb: " << a;
                cout << "\nc: " << c;
            }
            else
            {
                cout << "\nCannot do this much left shift!";
            }
        }
        else
        {
            cout << "\nWrong Input";
        }
    }
    else if (ch == 14)
    {
        int num;
        cout << "\na: " << a << "\nb: " << b;
        cout << "\nEnter How much you want to right shift?: ";
        cin >> num;
        cout << "\nWhich String?\n1)a or 2)b\nEnter(1 or 2): ";
        cin >> ch;
        if (ch == 1)
        {
            if (num < a.size())
            {
                STRING c;
                c = a >> num;
                cout << "\na: " << a;
                cout << "\nc: " << c;
            }
            else
            {
                cout << "\nCannot do this much right shift!";
            }
        }
        else if (ch == 2)
        {
            if (num < b.size())
            {
                STRING c;
                c = b >> num;
                cout << "\nb: " << b;
                cout << "\nc: " << c;
            }
            else
            {
                cout << "\nCannot do this much right shift!";
            }
        }
        else
        {
            cout << "\nWrong Input";
        }
    }
    else
    {
        cout << "Invalid Input!";
    }
    return 0;
}
