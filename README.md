    val inputList = List("\u0000@@Scala, 123!!\u0007", "\u001BSpark_#$%#$%#456$$\n", "\t%%Test789**\r")

    val cleanedList = inputList.map(_.replaceAll("^[^\\p{Print}a-zA-Z0-9]+|[^\\p{Print}a-zA-Z0-9]+$", ""))
    val cleanedList2 = inputList.map(_.trim.replaceAll("^[^a-zA-Z0-9]+|[^a-zA-Z0-9]+$", ""))
    val cleanedList3 = inputList.map(_.replaceAll("^[^\\p{Alnum}]+|[^\\p{Alnum}]+$", ""))
    println(inputList)
    println(cleanedList)  // Output: List(Scala123, Spark_456, Test789)
    println(cleanedList2)  // Output: List(Scala123, Spark_456, Test789)
    println(cleanedList3)
    
