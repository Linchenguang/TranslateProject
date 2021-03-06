为 Linux 初学者讲解 WC 命令(6个例子)
======

在命令行工作时，有时您可能想要访问一个文件中的单词数量、字节数、甚至换行数。如果您正在寻找这样做的工具，您会很高兴地知道，在 Linux 中，存在一个命令行实用程序，它被称为 -dubbed **wc** \-，它为您完成所有这些工作。在本文中，我们将通过简单易懂的例子来讨论这个工具。
但是在我们开始之前，值得一提的是，本教程中提供的所有示例都在 Ubuntu 16.04上进行了测试。
### Linux WC 命令

WC 命令打印每个输入文件的新行、字和字节数。以下是该命令行工具的语法:
```wc [OPTION]... [FILE]...```

以下是 WC 人工文档的解释:
```
Print newline, word, and byte counts for each FILE, and a total line if more than one FILE is
specified. A word is a non-zero-length sequence of characters delimited by white space. With no
FILE, or when FILE is -, read standard input.
为每个文件打印新行、单词和字节数，如果多于一个文件，则为总行指定。单词是由空格分隔的非零长度的字符序列。没有文件，或当文件为-，读取标准输入。
```

下面的 Q&A 样式的示例将会让您更好地了解 WC 命令的基本用法。
注意:在所有示例中我们将使用一个名为 ```file.txt``` 的文件作为输入文件。以下是该文件包含的内容:
```
hi
hello
how are you
thanks.
```

### Q1. 如何打印字节数

使用 **-c** 命令选项打印字节数.

**wc -c file.txt**

下面是这个命令在我们的系统上产生的输出:

[![如何打印字节数][1]][2]

文件包含29个字节。

### Q2. 如何打印字符数

要打印字符数，请使用 **-m** 命令行选项。
**wc -m file.txt**

下面是这个命令在我们的系统上产生的输出:

[![如何打印字符数][3]][4]

文件包含29个字符。

### Q3. 如何打印换行数

使用 **-l**命令选项来打印文件中的新行数。

**wc -l file.txt**

这里是我们的例子的输出:

[![如何打印换行数][5]][6]

### Q4. 如何打印字数

要打印文件中的单词数量，请使用 **-w**命令选项。

**wc -w file.txt**

在我们的例子中命令的输出如下:
[![如何打印字数][7]][8]

这显示文件中有6个单词。

### Q5. 如何打印最长行的显示宽度或长度

如果您想要打印输入文件中最长行的长度，请使用**-l**命令行选项。

**wc -L file.txt**

下面是在我们的案例中命令产生的结果:
[![如何打印最长行的显示宽度或长度][9]][10]

所以文件中最长的行长度是11。
### Q6. 如何从文件读取输入文件名

如果您有多个文件名，并且您希望 WC 从一个文件中读取它们，那么使用**\-files0-from**选项。
**wc --files0-from=names.txt**

[![如何从文件读取输入文件名][11]][12]

因此，您可以看到 WC 命令，在示例中，文件 **file.txt**输出了行、单词和字符数三种输出模式。文件名为 **file.txt**的文件在**name.txt**文件中提及。值得一提的是，为了成功地使用这个选项，写入文件的名称应该用 NUL 终止——您可以通过键入**Ctrl + v**然后按**Ctrl +Shift+ @**来生成这个字符。
### 结论

正如您所认同的一样，从理解和使用目的来看， WC 是一个简单的命令。我们已经介绍了几乎所有的命令行选项，所以您应该随时准备使用工具，在实践过程中以我们在这里解释过的内容为基础。想了解更多关于 WC 的信息，请参考它的[人工文档][13]。

--------------------------------------------------------------------------------

via: https://www.howtoforge.com/linux-wc-command-explained-for-beginners-6-examples/

作者：[Himanshu Arora][a]
译者：[stevenzdg988](https://github.com/stevenzdg988)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]:https://www.howtoforge.com
[1]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-c-option.png
[2]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-c-option.png
[3]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-m-option.png
[4]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-m-option.png
[5]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-l-option.png
[6]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-l-option.png
[7]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-w-option.png
[8]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-w-option.png
[9]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-L-option.png
[10]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-L-option.png
[11]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/wc-file0-from-option.png
[12]:https://www.howtoforge.com/images/usage_of_pfsense_to_block_dos_attack_/big/wc-file0-from-option.png
[13]:https://linux.die.net/man/1/wc
