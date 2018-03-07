# Programming #

LO:

- Basic principles of writing instructions in the form of programming code.
- What constants and variables are and how to use them.
- How to use useful variable names.
- A program is a list of instructions that a computer works though in a logical sequence to complete a task.
- Programming code is made up of algorithms that can be implemented within a programming language.
- An algorithm is a sequence of instructions, independent of any programming language, that can be followed to complete a task. Algorithms always terminate.
- Programming languages are used to write applications.

1st level language = Machine Code

2nd level language = Mnemonics

4th level language = High level

---------------

## My First Program ##

	Module VBModule
		Sub Main()
			Dim colour as String
			Console.WriteLine("What eyes have thee?")
			colour = Console.ReadLine().ToLower().Substring(0,5)
			'Console.WriteLine(colour)'
			If colour = "green" Then
				Console.WriteLine("Thou art a Goblin?")
			Else
				Console.WriteLine("Pray tell, be thou another form of beast?")
			End If
		End Sub
	  
	End Module

## My First Program - Expanded Edition! ##

	Module VBModule
		Sub Main()
			Dim colour as String
			Dim b as Boolean
			Dim passed as Boolean
			Dim inp as String
			Console.Write("What eyes have thee? ")
			colour = Console.ReadLine().ToLower().Substring(0,5)
			'Console.WriteLine(colour)'
			If colour = "green" Then
				Console.Write("Thou art a Goblin?" + Environment.NewLine + "(y/n)?")
				Do
					inp = Console.ReadLine()
					If inp.ToLower() = "y" Then
						inp = "True"
					ElseIf inp.ToLower() = "n" Then
						inp = "False"
					Else
						passed = False
						Console.Write("Not y or n!" + Environment.NewLine + "(y/n)?")
						Continue Do
					End If
					passed = Boolean.TryParse(inp,b)
				Loop Until passed
				'Console.WriteLine(passed)
				'Console.WriteLine(b)
				If b Then
					Console.WriteLine("Welcome to the hoarde. Zug zug!")
				Else
					Console.WriteLine("Go away, peasant!")
				End If
					
			Else
				Console.Write("Pray tell, what other beast art thou? ")
				Console.WriteLine("A '" & Console.ReadLine() &"'? Interesting...")
			End If
		End Sub
	  
	End Module
