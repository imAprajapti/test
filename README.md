{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "first f1 12\n",
      "first f1 13\n",
      "first f1 14\n"
     ]
    }
   ],
   "source": [
    "class test:\n",
    "    def f1(self,a):\n",
    "        self.a=a\n",
    "        print(\"first f1\",self.a)\n",
    "t1=test()#object 1\n",
    "t2=test()#object 2\n",
    "t3=test()#object 3\n",
    "t1.f1(12)\n",
    "t2.f1(13)\n",
    "t3.f1(14)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "12\n",
      "10\n"
     ]
    }
   ],
   "source": [
    "class test:\n",
    "    x=10\n",
    "    def __init__(self,x,y):\n",
    "        self.a=x\n",
    "        self.b=y\n",
    "t1=test(12,13)\n",
    "print(t1.a)\n",
    "print(t1.x)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "hello\n"
     ]
    }
   ],
   "source": [
    "class account:\n",
    "    x=10\n",
    "    def f1(self,a,b,c):\n",
    "        self.accno=a\n",
    "        self.balance=b\n",
    "        self.ifsc=c\n",
    "acc1=account()\n",
    "acc1.f1(1000,500000,'hello')\n",
    "print(acc1.ifsc)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "10\n",
      "hello arpit\n",
      "{'x': 12, 'y': 14}\n"
     ]
    }
   ],
   "source": [
    "class test:\n",
    "    x=10 #static variable\n",
    "    def __init__(self,a,b):  #init function\n",
    "        self.x=a\n",
    "        self.y=b\n",
    "        test.p=\"hello arpit\"   # p is also static variable created\n",
    "        print(test.p)\n",
    "print(test.x)\n",
    "t1=test(12,14)\n",
    "print(t1.__dict__)   #shows the instance variable created"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 64,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "26\n"
     ]
    }
   ],
   "source": [
    "class test:\n",
    "    def f1(self): #instance method\n",
    "        self.x=10\n",
    "    @staticmethod  # python will understand that this function is static method and will not consider first argument as static.\n",
    "    def f2(m,n):\n",
    "        ans=m+n\n",
    "        print(ans)\n",
    "test.f2(12,14)\n",
    "t1=test()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 82,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "swapped numbers are 34 25\n",
      "class method runs when class object calls 10 20\n",
      "{'x': 34, 'y': 25}\n"
     ]
    }
   ],
   "source": [
    "#program to swap two numbers using the opp's concept\n",
    "# program also showing the use of class method\n",
    "class test:\n",
    "    def __init__(self,a,b):\n",
    "        self.x=a   #instance variables\n",
    "        self.y=b   #instance variables\n",
    "        c=self.x\n",
    "        self.x=self.y\n",
    "        self.y=c\n",
    "        print(\"swapped numbers are\",self.x,self.y)\n",
    "    @classmethod   #by writing this function will be treated as the class method.\n",
    "    def f1(cls):   #default argument of class object i.e test will be passed to cls.\n",
    "        cls.x=10\n",
    "        cls.y=20\n",
    "        print(\"class method runs when class object calls\",cls.x,cls.y)\n",
    "obj=test(25,34)\n",
    "test.f1()\n",
    "print(obj.__dict__)\n",
    "        "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 87,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "f1 function runs 10\n",
      "20\n"
     ]
    }
   ],
   "source": [
    "# creating static variables outside the class\n",
    "class test:\n",
    "    def f1(self): #instance method\n",
    "        self.x=10\n",
    "        print(\"f1 function runs\",self.x)\n",
    "t1=test()\n",
    "t1.f1()\n",
    "test.y=20  #creating static variable outside the class\n",
    "print(test.y)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
