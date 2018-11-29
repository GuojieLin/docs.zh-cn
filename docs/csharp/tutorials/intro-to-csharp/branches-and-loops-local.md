---
title: 分支和循环 - C# 教程简介
description: 在本教程的“分支和循环”中，将编写 C# 代码以研究支持条件分支和循环重复执行语句的语言语法。
ms.date: 10/31/2017
ms.custom: mvc
ms.openlocfilehash: 0997c0b4a8f450c0e5eadc9616457a1ab84e7d96
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2018
ms.locfileid: "50186131"
---
# <a name="learn-conditional-logic-with-branch-and-loop-statements"></a><span data-ttu-id="627f2-103">通过分支和循环语句了解条件逻辑</span><span class="sxs-lookup"><span data-stu-id="627f2-103">Learn conditional logic with branch and loop statements</span></span>

<span data-ttu-id="627f2-104">本教程介绍了如何编写代码，从而检查变量，并根据这些变量更改执行路径。</span><span class="sxs-lookup"><span data-stu-id="627f2-104">This tutorial teaches you how to write code that examines variables and changes the execution path based on those variables.</span></span> <span data-ttu-id="627f2-105">读者可以编写 C# 代码并查看代码编译和运行结果。</span><span class="sxs-lookup"><span data-stu-id="627f2-105">You write C# code and see the results of compiling and running it.</span></span> <span data-ttu-id="627f2-106">本教程包含一系列课程，介绍了 C# 中的分支和循环构造。</span><span class="sxs-lookup"><span data-stu-id="627f2-106">The tutorial contains a series of lessons that explore branching and looping constructs in C#.</span></span> <span data-ttu-id="627f2-107">这些课程介绍了 C# 语言的基础知识。</span><span class="sxs-lookup"><span data-stu-id="627f2-107">These lessons teach you the fundamentals of the C# language.</span></span>

<span data-ttu-id="627f2-108">本教程要求你有一台可用于开发的计算机。</span><span class="sxs-lookup"><span data-stu-id="627f2-108">This tutorial expects you to have a machine you can use for development.</span></span> <span data-ttu-id="627f2-109">.NET 主题 [10 分钟入门](https://www.microsoft.com/net/core)介绍了如何在 Mac、PC 或 Linux 上设置本地开发环境。</span><span class="sxs-lookup"><span data-stu-id="627f2-109">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span> <span data-ttu-id="627f2-110">[熟悉开发工具](local-environment.md)不仅简要概述了将用到的命令，还收录了详细信息链接。</span><span class="sxs-lookup"><span data-stu-id="627f2-110">A quick overview of the commands you'll use is in the [Become familiar with the development tools](local-environment.md) with links to more details.</span></span>

## <a name="make-decisions-using-the-if-statement"></a><span data-ttu-id="627f2-111">使用 `if` 语句做出决定</span><span class="sxs-lookup"><span data-stu-id="627f2-111">Make decisions using the `if` statement</span></span>

<span data-ttu-id="627f2-112">创建名为 branches-tutorial 的目录。</span><span class="sxs-lookup"><span data-stu-id="627f2-112">Create a directory named **branches-tutorial**.</span></span> <span data-ttu-id="627f2-113">将新建的目录设为当前目录，并运行 `dotnet new console -n BranchesAndLoops -o .`。</span><span class="sxs-lookup"><span data-stu-id="627f2-113">Make that the current directory and run `dotnet new console -n BranchesAndLoops -o .`.</span></span> <span data-ttu-id="627f2-114">此命令会在当前目录中创建一个新的 .NET Core 控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="627f2-114">This command creates a new .NET Core console application in the current directory.</span></span>

<span data-ttu-id="627f2-115">在常用编辑器中，打开 Program.cs，并将行 `Console.Writeline("Hello World!");` 替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-115">Open **Program.cs** in your favorite editor, and replace the line `Console.Writeline("Hello World!");` with the following code:</span></span>

```csharp
int a = 5;
int b = 6;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10.");
```

<span data-ttu-id="627f2-116">通过在控制台窗口键入 `dotnet run` 试运行此代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-116">Try this code by typing `dotnet run` in your console window.</span></span> <span data-ttu-id="627f2-117">你应在控制台上看到以下消息：“The answer is greater than 10.</span><span class="sxs-lookup"><span data-stu-id="627f2-117">You should see the message "The answer is greater than 10."</span></span> <span data-ttu-id="627f2-118">（答案大于 10）”。</span><span class="sxs-lookup"><span data-stu-id="627f2-118">printed to your console.</span></span>

<span data-ttu-id="627f2-119">修改 `b` 的声明，让总和小于 10：</span><span class="sxs-lookup"><span data-stu-id="627f2-119">Modify the declaration of `b` so that the sum is less than 10:</span></span> 

```csharp
int b = 3;
```

<span data-ttu-id="627f2-120">再次键入 `dotnet run`。</span><span class="sxs-lookup"><span data-stu-id="627f2-120">Type `dotnet run` again.</span></span> <span data-ttu-id="627f2-121">由于答案小于 10，因此什么也没有打印出来。</span><span class="sxs-lookup"><span data-stu-id="627f2-121">Because the answer is less than 10, nothing is printed.</span></span> <span data-ttu-id="627f2-122">要测试的条件为 false。</span><span class="sxs-lookup"><span data-stu-id="627f2-122">The **condition** you're testing is false.</span></span> <span data-ttu-id="627f2-123">没有任何可供执行的代码，因为仅为 `if` 语句编写了一个可能分支，即 true 分支。</span><span class="sxs-lookup"><span data-stu-id="627f2-123">You don't have any code to execute because you've only written one of the possible branches for an `if` statement: the true branch.</span></span>

> [!TIP]
> <span data-ttu-id="627f2-124">在探索 C#（或任何编程语言）的过程中，可能会在编写代码时犯错。</span><span class="sxs-lookup"><span data-stu-id="627f2-124">As you explore C# (or any programming language), you'll make mistakes when you write code.</span></span> <span data-ttu-id="627f2-125">编译器会发现并报告这些错误。</span><span class="sxs-lookup"><span data-stu-id="627f2-125">The compiler will find and report the errors.</span></span> <span data-ttu-id="627f2-126">仔细查看错误输出和生成错误的代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-126">Look closely at the error output and the code that generated the error.</span></span> <span data-ttu-id="627f2-127">编译器错误通常可帮助你找出问题。</span><span class="sxs-lookup"><span data-stu-id="627f2-127">The compiler error can usually help you find the problem.</span></span>

<span data-ttu-id="627f2-128">第一个示例展示了 `if` 和布尔类型的用途。</span><span class="sxs-lookup"><span data-stu-id="627f2-128">This first sample shows the power of `if` and Boolean types.</span></span> <span data-ttu-id="627f2-129">布尔变量可以包含下列两个值之一：`true` 或 `false`。</span><span class="sxs-lookup"><span data-stu-id="627f2-129">A *Boolean* is a variable that can have one of two values: `true` or `false`.</span></span> <span data-ttu-id="627f2-130">C# 为布尔变量定义了特殊类型 `bool`。</span><span class="sxs-lookup"><span data-stu-id="627f2-130">C# defines a special type, `bool` for Boolean variables.</span></span> <span data-ttu-id="627f2-131">`if` 语句检查 `bool` 的值。</span><span class="sxs-lookup"><span data-stu-id="627f2-131">The `if` statement checks the value of a `bool`.</span></span> <span data-ttu-id="627f2-132">如果值为 `true`，执行 `if` 后面的语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-132">When the value is `true`, the statement following the `if` executes.</span></span> <span data-ttu-id="627f2-133">否则，跳过上述语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-133">Otherwise, it is skipped.</span></span>

<span data-ttu-id="627f2-134">这种检查条件并根据条件执行语句的过程非常强大。</span><span class="sxs-lookup"><span data-stu-id="627f2-134">This process of checking conditions and executing statements based on those conditions is very powerful.</span></span>

## <a name="make-if-and-else-work-together"></a><span data-ttu-id="627f2-135">让 if 和 else 完美配合</span><span class="sxs-lookup"><span data-stu-id="627f2-135">Make if and else work together</span></span>

<span data-ttu-id="627f2-136">若要执行 true 和 false 分支中的不同代码，请创建在条件为 false 时执行的 `else` 分支。</span><span class="sxs-lookup"><span data-stu-id="627f2-136">To execute different code in both the true and false branches, you create an `else` branch that executes when the condition is false.</span></span> <span data-ttu-id="627f2-137">试运行这些代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-137">Try this.</span></span> <span data-ttu-id="627f2-138">将以下代码中的最后两行添加到 `Main` 方法（你应该已经有前四个）：</span><span class="sxs-lookup"><span data-stu-id="627f2-138">Add the last two lines in the code below to your `Main` method (you should already have the first four):</span></span>

```csharp
int a = 5;
int b = 3;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10");
else
    Console.WriteLine("The answer is not greater than 10");
```

<span data-ttu-id="627f2-139">只有当条件的测试结果为 `false` 时，才执行 `else` 关键字后面的语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-139">The statement following the `else` keyword executes only when the condition being tested is `false`.</span></span> <span data-ttu-id="627f2-140">将 `if`、`else` 与布尔条件相结合，可以满足处理 `true` 和 `false` 所需的一切要求。</span><span class="sxs-lookup"><span data-stu-id="627f2-140">Combining `if` and `else` with Boolean conditions provides all the power you need to handle both a `true` and a `false` condition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="627f2-141">`if` 和 `else` 语句下的缩进是为了方便读者阅读。</span><span class="sxs-lookup"><span data-stu-id="627f2-141">The indentation under the `if` and `else` statements is for human readers.</span></span>
> <span data-ttu-id="627f2-142">C# 语言忽略缩进或空格。</span><span class="sxs-lookup"><span data-stu-id="627f2-142">The C# language doesn't treat indentation or white space as significant.</span></span> <span data-ttu-id="627f2-143">`if` 或 `else` 关键字后面的语句根据条件决定是否执行。</span><span class="sxs-lookup"><span data-stu-id="627f2-143">The statement following the `if` or `else` keyword will be executed based on the condition.</span></span> <span data-ttu-id="627f2-144">本教程中的所有示例都遵循了常见做法，根据语句的控制流缩进代码行。</span><span class="sxs-lookup"><span data-stu-id="627f2-144">All the samples in this tutorial follow a common practice to indent lines based on the control flow of statements.</span></span>

<span data-ttu-id="627f2-145">由于缩进会被忽略，因此需要使用 `{` 和 `}`，指明要在根据条件决定是否执行的代码块中添加多个语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-145">Because indentation is not significant, you need to use `{` and `}` to indicate when you want more than one statement to be part of the block that executes conditionally.</span></span> <span data-ttu-id="627f2-146">C# 程序员通常会对所有 `if` 和 `else` 子句使用这些大括号。</span><span class="sxs-lookup"><span data-stu-id="627f2-146">C# programmers typically use those braces on all `if` and `else` clauses.</span></span> <span data-ttu-id="627f2-147">以下示例与刚刚创建的示例相同。</span><span class="sxs-lookup"><span data-stu-id="627f2-147">The following example is the same as the one you just created.</span></span> <span data-ttu-id="627f2-148">修改上面的代码以匹配下面的代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-148">Modify your code above to match the following code:</span></span>

```csharp
int a = 5;
int b = 3;
if (a + b > 10)
{
    Console.WriteLine("The answer is greater than 10");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
}
```

> [!TIP]
> <span data-ttu-id="627f2-149">在本教程的其余部分中，代码示例全都遵循公认做法，添加了大括号。</span><span class="sxs-lookup"><span data-stu-id="627f2-149">Through the rest of this tutorial, the code samples all include the braces, following accepted practices.</span></span>

<span data-ttu-id="627f2-150">可以测试更复杂的条件。</span><span class="sxs-lookup"><span data-stu-id="627f2-150">You can test more complicated conditions.</span></span> <span data-ttu-id="627f2-151">在 `Main` 方法中，在当前已编写的代码之后添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-151">Add the following code in your `Main` method after the code you've written so far:</span></span>

```csharp
int c = 4;
if ((a + b + c > 10) && (a > b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("And the first number is greater than the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("Or the first number is not greater than the second");
}
```

<span data-ttu-id="627f2-152">`&&` 表示“且”。</span><span class="sxs-lookup"><span data-stu-id="627f2-152">The `&&` represents "and".</span></span> <span data-ttu-id="627f2-153">也就是说，两个条件必须都为 true，才能执行 true 分支中的语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-153">It means both conditions must be true to execute the statement in the true branch.</span></span>  <span data-ttu-id="627f2-154">这些示例还表明，可以在每个条件分支中添加多个语句，前提是将它们用 `{` 和 `}` 括住。</span><span class="sxs-lookup"><span data-stu-id="627f2-154">These examples also show that you can have multiple statements in each conditional branch, provided you enclose them in `{` and `}`.</span></span>

<span data-ttu-id="627f2-155">还可以使用 `||` 表示“或”。</span><span class="sxs-lookup"><span data-stu-id="627f2-155">You can also use  `||` to represent "or".</span></span> <span data-ttu-id="627f2-156">在当前已编写的代码之后添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-156">Add the following code after what you've written so far:</span></span>

```csharp
if ((a + b + c > 10) || (a > b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("Or the first number is greater than the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("And the first number is not greater than the second");
}
```

<span data-ttu-id="627f2-157">你已完成第一步。</span><span class="sxs-lookup"><span data-stu-id="627f2-157">You've finished the first step.</span></span> <span data-ttu-id="627f2-158">开始进入下一部分前，先将当前代码移到单独的方法中。</span><span class="sxs-lookup"><span data-stu-id="627f2-158">Before you start the next section, let's move the current code into a separate method.</span></span> <span data-ttu-id="627f2-159">这样一来，可以更轻松地开始处理新示例。</span><span class="sxs-lookup"><span data-stu-id="627f2-159">That makes it easier to start working with a new example.</span></span> <span data-ttu-id="627f2-160">将 `Main` 方法重命名为 `ExploreIf`，并编写调用 `ExploreIf` 的新 `Main` 方法。</span><span class="sxs-lookup"><span data-stu-id="627f2-160">Rename your `Main` method to `ExploreIf` and write a new `Main` method that calls `ExploreIf`.</span></span> <span data-ttu-id="627f2-161">完成后，代码应如下所示：</span><span class="sxs-lookup"><span data-stu-id="627f2-161">When you have finished, your code should look like this:</span></span>

```csharp
using System;

namespace BranchesAndLoops
{
    class Program
    {
        static void ExploreIf()
        {
            int a = 5;
            int b = 3;
            if (a + b > 10)
            {
                Console.WriteLine("The answer is greater than 10");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
            }

            if ((a + b + c > 10) && (a > b))
            {
                Console.WriteLine("The answer is greater than 10");
                Console.WriteLine("And the first number is greater than the second");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
                Console.WriteLine("Or the first number is not greater than the second");
            }

            if ((a + b + c > 10) || (a > b))
            {
                Console.WriteLine("The answer is greater than 10");
                Console.WriteLine("Or the first number is greater than the second");
            }
            else
            {
                Console.WriteLine("The answer is not greater than 10");
                Console.WriteLine("And the first number is not greater than the second");
            }            
        }

        static void Main(string[] args)
        {
            ExploreIf();
        }
    }
}
```

<span data-ttu-id="627f2-162">注释掉对 `ExploreIf()` 的调用。</span><span class="sxs-lookup"><span data-stu-id="627f2-162">Comment out the call to `ExploreIf()`.</span></span> <span data-ttu-id="627f2-163">在本节中，它会在你工作时使输出变得不那么杂乱：</span><span class="sxs-lookup"><span data-stu-id="627f2-163">It will make the output less cluttered as you work in this section:</span></span>

```csharp
//ExploreIf();
```

<span data-ttu-id="627f2-164">`//` 在 C# 中启动 注释。</span><span class="sxs-lookup"><span data-stu-id="627f2-164">The `//` starts a **comment** in C#.</span></span> <span data-ttu-id="627f2-165">注释是你想要保留在源代码中但不能作为代码执行的任何文本。</span><span class="sxs-lookup"><span data-stu-id="627f2-165">Comments are any text you want to keep in your source code but not execute as code.</span></span> <span data-ttu-id="627f2-166">编译器不会从注释中生成任何可执行代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-166">The compiler does not generate any executable code from comments.</span></span>

## <a name="use-loops-to-repeat-operations"></a><span data-ttu-id="627f2-167">使用循环重复执行运算</span><span class="sxs-lookup"><span data-stu-id="627f2-167">Use loops to repeat operations</span></span>

<span data-ttu-id="627f2-168">在本节使用循环以重复执行语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-168">In this section you use **loops** to repeat statements.</span></span> <span data-ttu-id="627f2-169">请在 `Main` 方法中试用以下代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-169">Try this code in your `Main` method:</span></span>

```csharp
int counter = 0;
while (counter < 10)
{
    Console.WriteLine($"Hello World! The counter is {counter}");
    counter++;
}
```

<span data-ttu-id="627f2-170">`while` 语句会检查条件，并执行 `while` 后面的语句或语句块。</span><span class="sxs-lookup"><span data-stu-id="627f2-170">The `while` statement checks a condition and executes the statement or statement block following the `while`.</span></span> <span data-ttu-id="627f2-171">除非条件为 false，否则它会重复检查条件并执行这些语句。</span><span class="sxs-lookup"><span data-stu-id="627f2-171">It repeatedly checks the condition and executing those statements until the condition is false.</span></span>

<span data-ttu-id="627f2-172">此示例新引入了另外一个运算符。</span><span class="sxs-lookup"><span data-stu-id="627f2-172">There's one other new operator in this example.</span></span> <span data-ttu-id="627f2-173">`counter` 变量后面的 `++` 是增量运算符。</span><span class="sxs-lookup"><span data-stu-id="627f2-173">The `++` after the `counter` variable is the **increment** operator.</span></span> <span data-ttu-id="627f2-174">它将 `counter` 值加 1，并将计算后的值存储在 `counter` 变量中。</span><span class="sxs-lookup"><span data-stu-id="627f2-174">It adds 1 to the value of `counter` and stores that value in the `counter` variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="627f2-175">请确保 `while` 循环条件在你执行代码时更改为 false。</span><span class="sxs-lookup"><span data-stu-id="627f2-175">Make sure that the `while` loop condition changes to false as you execute the code.</span></span> <span data-ttu-id="627f2-176">否则，创建的就是无限循环，即程序永不结束。</span><span class="sxs-lookup"><span data-stu-id="627f2-176">Otherwise, you create an **infinite loop** where your program never ends.</span></span> <span data-ttu-id="627f2-177">本示例中没有演示上述情况，因为你必须使用 CTRL-C 或其他方法强制退出程序。</span><span class="sxs-lookup"><span data-stu-id="627f2-177">That is not demonstrated in this sample, because you have to force your program to quit using **CTRL-C** or other means.</span></span>

<span data-ttu-id="627f2-178">`while` 循环先测试条件，然后再执行 `while` 后面的代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-178">The `while` loop tests the condition before executing the code following the `while`.</span></span> <span data-ttu-id="627f2-179">`do` ... `while` 循环先执行代码，然后再检查条件。</span><span class="sxs-lookup"><span data-stu-id="627f2-179">The `do` ... `while` loop executes the code first, and then checks the condition.</span></span> <span data-ttu-id="627f2-180">下面的代码对 Do While 循环进行了演示：</span><span class="sxs-lookup"><span data-stu-id="627f2-180">The do while loop is shown in the following code:</span></span>

```csharp
counter = 0;
do
{
    Console.WriteLine($"Hello World! The counter is {counter}");
    counter++;
} while (counter < 10);
```

<span data-ttu-id="627f2-181">此 `do` 循环和前面的 `while` 循环生成的输出结果相同。</span><span class="sxs-lookup"><span data-stu-id="627f2-181">This `do` loop and the earlier `while` loop produce the same output.</span></span>

## <a name="work-with-the-for-loop"></a><span data-ttu-id="627f2-182">使用 for 循环</span><span class="sxs-lookup"><span data-stu-id="627f2-182">Work with the for loop</span></span>

<span data-ttu-id="627f2-183">For 循环通常用在 C# 中。</span><span class="sxs-lookup"><span data-stu-id="627f2-183">The **for** loop is commonly used in C#.</span></span> <span data-ttu-id="627f2-184">请在 Main() 方法中试用以下代码：</span><span class="sxs-lookup"><span data-stu-id="627f2-184">Try this code in your Main() method:</span></span>

```csharp
for(int index = 0; index < 10; index++)
{
    Console.WriteLine($"Hello World! The index is {index}");
} 
```

<span data-ttu-id="627f2-185">此循环的工作原理与已用过的 `while` 循环和 `do` 循环相同。</span><span class="sxs-lookup"><span data-stu-id="627f2-185">This does the same work as the `while` loop and the `do` loop you've already used.</span></span> <span data-ttu-id="627f2-186">`for` 语句包含三个控制具体工作方式的部分。</span><span class="sxs-lookup"><span data-stu-id="627f2-186">The `for` statement has three parts that control how it works.</span></span>

<span data-ttu-id="627f2-187">第一部分是 for 初始值设定项：`for index = 0;` 声明 `index` 是循环变量，并将它的初始值设置为 `0`。</span><span class="sxs-lookup"><span data-stu-id="627f2-187">The first part is the **for initializer**: `for index = 0;` declares that `index` is the loop variable, and sets its initial value to `0`.</span></span>

<span data-ttu-id="627f2-188">中间部分是 for 条件：`index < 10` 声明只要计数器值小于 10，此 `for` 循环就会继续执行。</span><span class="sxs-lookup"><span data-stu-id="627f2-188">The middle part is the **for condition**: `index < 10` declares that this `for` loop continues to execute as long as the value of counter is less than 10.</span></span>

<span data-ttu-id="627f2-189">最后一部分是 for 迭代器：`index++` 指定在执行 `for` 语句后面的代码块后，如何修改循环变量。</span><span class="sxs-lookup"><span data-stu-id="627f2-189">The final part is the **for iterator**: `index++` specifies how to modify the loop variable after executing the block following the `for` statement.</span></span> <span data-ttu-id="627f2-190">在此示例中，它指定 `index` 应在代码块每次执行时递增 1。</span><span class="sxs-lookup"><span data-stu-id="627f2-190">Here, it specifies that `index` should be incremented by 1 each time the block executes.</span></span>

<span data-ttu-id="627f2-191">亲自试运行这些部分的代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-191">Experiment with these yourself.</span></span> <span data-ttu-id="627f2-192">试着执行下列两项操作：</span><span class="sxs-lookup"><span data-stu-id="627f2-192">Try each of the following:</span></span>

- <span data-ttu-id="627f2-193">将初始值设定项更改为其他初始值。</span><span class="sxs-lookup"><span data-stu-id="627f2-193">Change the initializer to start at a different value.</span></span>
- <span data-ttu-id="627f2-194">将结束条件设定项更改为其他值。</span><span class="sxs-lookup"><span data-stu-id="627f2-194">Change the condition to stop at a different value.</span></span>

<span data-ttu-id="627f2-195">完成后，继续利用所学知识，试着自己编写一些代码。</span><span class="sxs-lookup"><span data-stu-id="627f2-195">When you're done, let's move on to write some code yourself to use what you've learned.</span></span>

## <a name="combine-branches-and-loops"></a><span data-ttu-id="627f2-196">结合使用分支和循环</span><span class="sxs-lookup"><span data-stu-id="627f2-196">Combine branches and loops</span></span>

<span data-ttu-id="627f2-197">支持，大家已了解 C# 语言中的 `if` 语句和循环构造。看看能否编写 C# 代码，计算 1 到 20 中所有可被 3 整除的整数的总和。</span><span class="sxs-lookup"><span data-stu-id="627f2-197">Now that you've seen the `if` statement and the looping constructs in the C# language, see if you can write C# code to find the sum of all integers 1 through 20 that are divisible by 3.</span></span>  <span data-ttu-id="627f2-198">下面提供了一些提示：</span><span class="sxs-lookup"><span data-stu-id="627f2-198">Here are a few hints:</span></span>

- <span data-ttu-id="627f2-199">`%` 运算符可用于获取除法运算的余数。</span><span class="sxs-lookup"><span data-stu-id="627f2-199">The `%` operator gives you the remainder of a division operation.</span></span>
- <span data-ttu-id="627f2-200">`if` 语句中的条件可用于判断是否应将数字计入总和。</span><span class="sxs-lookup"><span data-stu-id="627f2-200">The `if` statement gives you the condition to see if a number should be part of the sum.</span></span>
- <span data-ttu-id="627f2-201">`for` 循环有助于对 1 到 20 中的所有数字重复执行一系列步骤。</span><span class="sxs-lookup"><span data-stu-id="627f2-201">The `for` loop can help you repeat a series of steps for all the numbers 1 through 20.</span></span>

<span data-ttu-id="627f2-202">亲自试一试吧。</span><span class="sxs-lookup"><span data-stu-id="627f2-202">Try it yourself.</span></span> <span data-ttu-id="627f2-203">然后，看看自己是怎么做到的。</span><span class="sxs-lookup"><span data-stu-id="627f2-203">Then check how you did.</span></span> <span data-ttu-id="627f2-204">你应获取的答案为 63。</span><span class="sxs-lookup"><span data-stu-id="627f2-204">You should get 63 for an answer.</span></span> <span data-ttu-id="627f2-205">通过[在 GitHub 上查看已完成的代码](https://github.com/dotnet/samples/tree/master/csharp/branches-quickstart/Program.cs#L46-L54)，你可以看到一个可能的答案。</span><span class="sxs-lookup"><span data-stu-id="627f2-205">You can see one possible answer by [viewing the completed code on GitHub](https://github.com/dotnet/samples/tree/master/csharp/branches-quickstart/Program.cs#L46-L54).</span></span>

<span data-ttu-id="627f2-206">已完成“分支和循环”教程。</span><span class="sxs-lookup"><span data-stu-id="627f2-206">You've completed the "branches and loops" tutorial.</span></span>

<span data-ttu-id="627f2-207">你可继续在自己的开发环境中学习[字符串内插](interpolated-strings-local.md)教程。</span><span class="sxs-lookup"><span data-stu-id="627f2-207">You can continue with the [String interpolation](interpolated-strings-local.md) tutorial in your own development environment.</span></span>

<span data-ttu-id="627f2-208">若要详细了解这些概念，请参阅下列主题：</span><span class="sxs-lookup"><span data-stu-id="627f2-208">You can learn more about these concepts in these topics:</span></span>

[<span data-ttu-id="627f2-209">If 和 else 语句</span><span class="sxs-lookup"><span data-stu-id="627f2-209">If and else statement</span></span>](../../language-reference/keywords/if-else.md)  
[<span data-ttu-id="627f2-210">While 语句</span><span class="sxs-lookup"><span data-stu-id="627f2-210">While statement</span></span>](../../language-reference/keywords/while.md)  
[<span data-ttu-id="627f2-211">Do 语句</span><span class="sxs-lookup"><span data-stu-id="627f2-211">Do statement</span></span>](../../language-reference/keywords/do.md)  
[<span data-ttu-id="627f2-212">For 语句</span><span class="sxs-lookup"><span data-stu-id="627f2-212">For statement</span></span>](../../language-reference/keywords/for.md)  