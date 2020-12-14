fun main(){
    //variabel
    val firstname1 = "Andi"
    val lastname1 = "Budiman"
    val age1 = 34

    println(firstname1)
    println(lastname1)
    println(age1)

    val firstname2 = "Rudi"
    val lastname2 = "Setiawan"
    val age2 = "25"

    println(firstname2)
    println(lastname2)
    println(age2)

    //array
    val firstName = arrayListOf<String>()
    val lastname = arrayListOf<String>()
    val age = arrayListOf<Int>()

    firstName.add("Andi")
    lastname.add("Budiman")
    age.add(34)

    firstName.add("Budi")
    lastname.add("Setiawan")
    age.add(25)

    for (first in firstName){
        println(first)
    }
    for (last in lastname){
        println(last)
    }
    for (a in age){
        println(a)
    }

    //array v2
    val andiArray = arrayListOf<Any>()
    andiArray.add("Andi")
    andiArray.add("Budiman")
    andiArray.add(34)
    for (andi in andiArray){
        println(andi)
    }

    //array v3
    val mhsArray = arrayListOf<ArrayList<Any>>()
    mhsArray.add(andiArray)
    mhsArray.add(arrayListOf("Rudi", "Setiawan", 25))
    for (item in mhsArray){
        for (i in item){
            println(i)
        }
    }

    //data class
    val andi = User(firstName = "Andi", lastName = "Budiman", age = 34)
    val rudi = User(age = 25, lastName = "Setiawan", firstName = "Rudi")
    val dedi = User()
    dedi.age = 35
    dedi.firstName = "Dedi"

    val andi2 = andi.copy(age = 48)

    println(andi)
    println(rudi)
    println(dedi)

    println(andi.lastName)
    println(andi2)

    //data class array
    val mhsAmikom = arrayListOf<User>()
    mhsAmikom.add(andi)
    mhsAmikom.add(rudi)
    mhsAmikom.add(dedi)

    mhsAmikom.add(User(firstName = "Ferdi", lastName = "Setiawan", age = 45))

    for (mhs in mhsAmikom){
        println(mhs)
    }
}