{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "4_廻圈loop.ipynb",
      "provenance": [],
      "collapsed_sections": [
        "9XUenoirDtcm"
      ]
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9XUenoirDtcm"
      },
      "source": [
        "## 課程目標：\n",
        "```\n",
        "[1].使用range 函式 的功能建立整數循序數列\n",
        "\n",
        "[2].使用for 廻圈 執行固定次數的廻圈運算(通常)\n",
        "[3].使用while 廻圈執行沒有固定次數的廻圈運算\n",
        "\n",
        "[4].continue 指令 \n",
        "  是在廻圈執行中途暫時停住不往下執行，而跳到廻圈的起始處執行\n",
        "[5].break 指令:可在廻圈執行中途強迫跳離廻圈，跳到廻圈後面的程式繼續執行。\n",
        "\n",
        "[6].廻圈中又包含廻圈的巢狀廻圈(Nested Loop)　===>設計九九乘法表\n",
        "```\n",
        "```\n",
        "PS:Python沒有do… while 廻圈\n",
        "你自己實作一個吧?!!\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "jjZwT3gGD6CV"
      },
      "source": [
        "# 1.range() 函式\n",
        "```\n",
        " 使用range 函式 的建立整數循序數列\n",
        " \n",
        "變數1 = range(整數值)\n",
        "變數2 = range(起始值, 終止值)\n",
        "變數3 = range(起始值, 終止值, 多少間隔)\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "PYzbQkN3EB37"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "list1=range(10)\n",
        "print(list1)\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "lH9WI63pDswj",
        "outputId": "71864a62-5e44-40a8-9215-0de0a75bae4f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 35
        }
      },
      "source": [
        "list1=range(10)\n",
        "print(list1)"
      ],
      "execution_count": 2,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "range(0, 10)\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "26K6a6e2EQoL"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "list1=range(10)\n",
        "print(list1)\n",
        "\n",
        "print(list(list1))\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "eiv5LVu1EaAJ",
        "outputId": "52618b75-bf74-4d24-a188-7e23dd6cca65",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 52
        }
      },
      "source": [
        "list1=range(10)\n",
        "print(list1)\n",
        "\n",
        "print(list(list1))"
      ],
      "execution_count": 3,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "range(0, 10)\n",
            "[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "L4h35BhIEfSy"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "list2=range(-4,5)\n",
        "print(list(list2))\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "NCvYIEV4Ektk",
        "outputId": "de663032-69a5-4e4a-eef8-c640e9728328",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 35
        }
      },
      "source": [
        "list2=range(-4,5)\n",
        "print(list(list2))"
      ],
      "execution_count": 4,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[-4, -3, -2, -1, 0, 1, 2, 3, 4]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "8dydXXXcEqsL"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "list3=range(-4,5,2)\n",
        "print(list(list3))\n",
        "```\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8BA2ayFPEwIr",
        "outputId": "f8dd7458-898b-4708-95f6-01dd166e75a6",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 35
        }
      },
      "source": [
        "list3=range(-4,5,2)\n",
        "print(list(list3))"
      ],
      "execution_count": 5,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[-4, -2, 0, 2, 4]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "iQ7yqm-DE5UD"
      },
      "source": [
        "# [2]for 廻圈\n",
        "```\n",
        "使用for 廻圈 執行固定次數的廻圈運算(通常)\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9SOyhJKEE8IT"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "for n in range(5):\n",
        "  print(n)\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "FVl9RgsbFIk7",
        "outputId": "c2be86ba-b725-4bbf-ee71-c01d4b0cb612",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 105
        }
      },
      "source": [
        "for n in range(5):\n",
        "  print(n)"
      ],
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0\n",
            "1\n",
            "2\n",
            "3\n",
            "4\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Mwkc55eeFY8L"
      },
      "source": [
        "### 作業:印出底下range(5)數字\n",
        "```\n",
        "0 1 2 3 4\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "gmsFaJWmFuZf",
        "outputId": "f1548c54-11d5-42fd-bf16-1b091297bbb2",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "for n in range(5):\n",
        "    print(n, end=' ')"
      ],
      "execution_count": 9,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0 1 2 3 4 "
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "57NB1uKFFSVL"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "for n in range(10):\n",
        "    print(n, end='@')\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "1oDqFY5fFWb1",
        "outputId": "8e515d93-c4d1-4a2c-a666-36c3ef2c61b0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "for n in range(10):\n",
        "    print(n, end='@')"
      ],
      "execution_count": 7,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0@1@2@3@4@5@6@7@8@9@"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "dR5vPIKXF8xc",
        "outputId": "7710c8e7-75ee-45c1-ac5b-95091dee0f98",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "for n in range(10):\n",
        "   print(n, end='%%%%')"
      ],
      "execution_count": 10,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0%%%%1%%%%2%%%%3%%%%4%%%%5%%%%6%%%%7%%%%8%%%%9%%%%"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "WypPvxtcGO4R"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "mysum = 0\n",
        "\n",
        "for n in range(5):\n",
        "  mysum += n\n",
        "  print(mysum)\n",
        "```\n",
        "```\n",
        "mysum += n\n",
        "就是\n",
        "mysum = mysum + n\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "SLxFCBQSGZSB",
        "outputId": "d4034b1d-d91d-4029-b6dd-e743dabafa64",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 103
        }
      },
      "source": [
        "mysum = 0\n",
        "\n",
        "for n in range(5):\n",
        "  mysum += n\n",
        "  print(mysum)"
      ],
      "execution_count": 11,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0\n",
            "1\n",
            "3\n",
            "6\n",
            "10\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "1pYgf0TSGeQD"
      },
      "source": [
        "底下程式執行後結果為何?\n",
        "```\n",
        "mysum = 0\n",
        "\n",
        "for n in range(5):\n",
        "  mysum += n\n",
        "  \n",
        "print(mysum)\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "c-DotU51Hikc"
      },
      "source": [
        "## [程式閱讀題]\n",
        "```\n",
        "執行下列程式並說明其結果\n",
        "\n",
        "numbers = [21, 4, 35, 1, 8, 7, 3, 6, 9]\n",
        "my_numbers = []\n",
        "\n",
        "for number in numbers:\n",
        "  if (number % 2 != 0): \n",
        "    my_numbers.append(number)\n",
        "\n",
        "print(my_numbers)\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "aJCgzmqtH2FB",
        "outputId": "9b57198d-d27e-4f02-da4f-d86e3f98d2f8",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "numbers = [21, 4, 35, 1, 8, 7, 3, 6, 9]\n",
        "my_numbers = []\n",
        "\n",
        "for number in numbers:\n",
        "  if (number % 2 != 0): \n",
        "    my_numbers.append(number)\n",
        "\n",
        "print(my_numbers)"
      ],
      "execution_count": 12,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[21, 35, 1, 7, 3, 9]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "YEZ0Y4XwHqmd"
      },
      "source": [
        "### [程式閱讀題]\n",
        "上述程式如果第五行改成  if (number % 2 = 0):答案會是甚麼??"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "-Q8nUklLIclr"
      },
      "source": [
        "## [程式填充題]\n",
        "```\n",
        "下列程式將某LIST中的奇數挑出\n",
        "\n",
        "請完成其中填空\n",
        "\n",
        "numbers = [21, 4, 35, 1, 8, 7, 3, 6, 9]\n",
        "my_numbers = []\n",
        "\n",
        "for number in numbers:\n",
        "  if _______________: \n",
        "    my_numbers.append(number)\n",
        "\n",
        "print(my_numbers)\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "A_kJIyfDI4y1"
      },
      "source": [
        "# [3]While Loop\n",
        "```\n",
        "n階程的計算:n!=1*2*3*⋯*n\n",
        "1!　=　１\n",
        "2!　=　1*2　=　2\n",
        "3!　=　1*2*3　=　6\n",
        "\n",
        "輸入::一個正整數 n\n",
        "輸出::n!\n",
        "\n",
        "當使用者輸入一個正整數 n 後，\n",
        "程式就會顯示1*2*3*...*n 的乘積\n",
        "請使用 while loop設計這個程式\n",
        "```"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "C2b-kp1kJa_c"
      },
      "source": [
        "# [程式填充題]\n",
        "\n",
        "下列程式為n階程的計算\n",
        " \n",
        "請完成其中填空\n",
        "```\n",
        "total = 1\n",
        "i = 1\n",
        "\n",
        "n = int(input(\"請輸入正整數 n 的值：\"))\n",
        "\n",
        "while(i<=n):\n",
        "    ___________________ \n",
        "    ___________________      \n",
        "\n",
        "print(\"%d!=%d\" % (n, total))\n",
        "```"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ToUYMCTWJF_B",
        "outputId": "cefc1f30-c9f4-4289-b917-04d28c65a289",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "total = 1\n",
        "i = 1\n",
        "\n",
        "n = int(input(\"請輸入正整數 n 的值：\"))\n",
        "\n",
        "while(i<=n):\n",
        "    total *= i  \n",
        "    i+=1      \n",
        "\n",
        "print(\"%d!=%d\" % (n, total))"
      ],
      "execution_count": 13,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "請輸入正整數 n 的值：3\n",
            "3!=6\n"
          ],
          "name": "stdout"
        }
      ]
    }
  ]
}
