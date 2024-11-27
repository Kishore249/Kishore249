
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "!pip install qrcode"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [],
   "source": [
    "from PIL import Image, ImageDraw, ImageFont\n",
    "import random\n",
    "import os\n",
    "import datetime\n",
    "import qrcode"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "image = Image.new('RGB', (1000,900), (255, 255, 255))\n",
    "draw = ImageDraw.Draw(image)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "font = ImageFont.truetype('arial.ttf', size=45)\n",
    "os.system(\"ID CARD Generator\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "13-12-2020\t ID CARD Generator\t  06:02:02 PM\n"
     ]
    }
   ],
   "source": [
    "d_date = datetime.datetime.now()\n",
    "reg_format_date = d_date.strftime(\"%d-%m-%Y\\t ID CARD Generator\\t  %I:%M:%S %p\")\n",
    "print (reg_format_date)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "\n",
      "All Fields are Mandatory\n",
      "Avoid any kind of Spelling Mistakes\n",
      "Write Everything in uppercase letters\n",
      "\n",
      "Enter Your Company Name: Amazon\n"
     ]
    }
   ],
   "source": [
    "print('\\n\\nAll Fields are Mandatory') \n",
    "print('Avoid any kind of Spelling Mistakes')\n",
    "print('Write Everything in uppercase letters')\n",
    "(x, y) = (50, 50)\n",
    "message = input('\\nEnter Your Company Name: ')\n",
    "company=message\n",
    "color = 'rgb(0, 0, 0)'\n",
    "font = ImageFont.truetype('arial.ttf', size=80)\n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [],
   "source": [
    "# adding an unique id number. You can manually take it from user\n",
    "(x, y) = (600, 75)\n",
    "idno=random.randint(10000000,90000000)\n",
    "message = str('ID '+str(idno))\n",
    "color = 'rgb(0, 0, 0)' # black color\n",
    "font = ImageFont.truetype('arial.ttf', size=60)\n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Full Name: Kamalesh Karthi\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 250)\n",
    "message = input('Enter Your Full Name: ')\n",
    "name=message\n",
    "color = 'rgb(0, 0, 0)' # black color\n",
    "font = ImageFont.truetype('arial.ttf', size=45)\n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Gender: Male\n",
      "Enter Your Age: 25\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 350)\n",
    "message = input('Enter Your Gender: ')\n",
    "color = 'rgb(0, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)\n",
    "(x, y) = (250, 350)\n",
    "message = input('Enter Your Age: ')\n",
    "color = 'rgb(0, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Date Of Birth: 14/07/1995\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 450)\n",
    "message = input('Enter Your Date Of Birth: ')\n",
    "color = 'rgb(0, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Blood Group: O+\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 550)\n",
    "message = input('Enter Your Blood Group: ')\n",
    "color = 'rgb(255, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Mobile Number: 987654321\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 650)\n",
    "message = input('Enter Your Mobile Number: ')\n",
    "temp=message\n",
    "color = 'rgb(0, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter Your Address: Tamil Nadu\n"
     ]
    }
   ],
   "source": [
    "(x, y) = (50, 750)\n",
    "message = input('Enter Your Address: ')\n",
    "color = 'rgb(0, 0, 0)' # black color \n",
    "draw.text((x, y), message, fill=color, font=font)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [],
   "source": [
    "image.save(str(name)+'.png')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [],
   "source": [
    "img = qrcode.make(str(company)+str(idno))   # this info. is added in QR code, also add other things\n",
    "img.save(str(idno)+'.bmp')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [],
   "source": [
    "til = Image.open(name+'.png')\n",
    "im = Image.open(str(idno)+'.bmp') #25x25\n",
    "til.paste(im,(600,350))\n",
    "til.save(name+'.png')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "\n",
      "\n",
      "Your ID Card Successfully created in a PNG file Kamalesh Karthi.png\n",
      "\n",
      "\n",
      "Press any key to Close program...f\n"
     ]
    },
    {
     "ename": "NameError",
     "evalue": "name 'f' is not defined",
     "output_type": "error",
     "traceback": [
      "\u001b[1;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[1;31mNameError\u001b[0m                                 Traceback (most recent call last)",
      "\u001b[1;32m<ipython-input-17-50a1aea72307>\u001b[0m in \u001b[0;36m<module>\u001b[1;34m\u001b[0m\n\u001b[0;32m      1\u001b[0m \u001b[0mprint\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;34m'\\n\\n\\nYour ID Card Successfully created in a PNG file '\u001b[0m\u001b[1;33m+\u001b[0m\u001b[0mname\u001b[0m\u001b[1;33m+\u001b[0m\u001b[1;34m'.png'\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m\u001b[0m\u001b[1;33m\u001b[0m\u001b[0m\n\u001b[1;32m----> 2\u001b[1;33m \u001b[0meval\u001b[0m\u001b[1;33m(\u001b[0m\u001b[0minput\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;34m'\\n\\nPress any key to Close program...'\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m\u001b[0m\u001b[1;33m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[1;32m<string>\u001b[0m in \u001b[0;36m<module>\u001b[1;34m\u001b[0m\n",
      "\u001b[1;31mNameError\u001b[0m: name 'f' is not defined"
     ]
    }
   ],
   "source": [
    "print(('\\n\\n\\nYour ID Card Successfully created in a PNG file '+name+'.png'))\n",
    "eval(input('\\n\\nPress any key to Close program...'))"
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
   "version": "3.6.10"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
