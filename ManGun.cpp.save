struct Mangun
{
    int x;
    int y;
    int width;
    int height;
    int hp;
    int kadr;
    HDC Right;
    HDC Left;
    HDC picture;
    char LEFT;
    char RIGHT;
    char UP;
    char DOWN;
};
void drawMan(Mangun mangun1)
{
    txTransparentBlt (txDC(), mangun1.x, mangun1.y, mangun1.width, mangun1.height, mangun1.picture, mangun1.width * mangun1.kadr, 0, TX_WHITE);
    txSetFillColor(TX_WHITE);
    txRectangle(mangun1.x, mangun1.y - 30, mangun1.x + 100, mangun1.y - 10);
    txSetFillColor(TX_GREEN);
    txRectangle(mangun1.x, mangun1.y - 30, mangun1.x + 10 * mangun1.hp, mangun1.y - 10);
}

HDC changeMangunPic(Mangun mangun1)
{
    if (GetAsyncKeyState(mangun1.LEFT))
    {
        mangun1.picture = mangun1.Left;
    }
    if (GetAsyncKeyState(mangun1.RIGHT))
    {
        mangun1.picture = mangun1.Right;
    }

    return mangun1.picture;
}

void checkBorders(int *x2, int *y2, int width, int height)
{

    if (*x2 < 0)
    {
       *x2 = 0;
    }
    else if (*x2 + width > txGetExtentX())
    {
       *x2 = txGetExtentX() - width;
    }

    if (*y2 < 0)
    {
        *y2 = 0;
    }
    else if (*y2 + height > txGetExtentY())
    {
        *y2 = txGetExtentY() - height;
    }

}
void moveMangun(int *x_mangun, int *y_mangun, int *kadr1, char UP, char DOWN)
{

    //Движение
    if (GetAsyncKeyState(UP))
    {
        *y_mangun = *y_mangun  -10;
    }
    else if (GetAsyncKeyState(DOWN))
    {
       *y_mangun = *y_mangun  +10;
    }

    if (*kadr1 >= 2)
    {
        *kadr1 = 0;
    }

    //Столкновение с границами
    checkBorders(x_mangun, y_mangun, 150, 150);
}
void moveMangun2(int *x_mangun3,int *y_mangun3, int *kadr3,char UP, char DOWN)
{
        //Движение
        if (GetAsyncKeyState('6'))
        {
            *y_mangun3 = *y_mangun3  -10;
        }
        else if (GetAsyncKeyState('5'))
        {
            *y_mangun3 = *y_mangun3  +10;
        }

        if (*kadr3 >= 2)
        {
            *kadr3 = 0;
        }


        //Столкновение с границами
        checkBorders(x_mangun3, y_mangun3, 150, 150);
}
