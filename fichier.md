# Résume langage Ruby
## Les classes des objets
  * Le type String
  ```ruby
    "abcd".class #=> String
  ```
   Exemple des methode
  ```ruby
    "abcd".length #=> 4
    "abcd".count  #=> 4
    "abcd".empty? #=> false
    "abcd".count('b') #=> 1
    "abcd".insert(3, "gh") #=> abcghd
    "abcd".upcase #=> ABCD
    "ABCD".downcase #=> abcd
    "ABCD".capitalize #=> Abcd
    "15".to_i #=> 15 # integer
     a = "abcde"  a.clear    #=> ""
    "Hello, how are you?".split #=> ["Hello,", "how", "are", "you?"]
    "H-e-l-l-o".split('-') #=> ["H", "e", "l", "l", "o"]
  ```
  * La classe Integer
   ```ruby
    123.class #=> Integer
   ```
  Exemple des methodes:
  ```ruby
    15.even? #=> false
    4.even? #=> true
    15.odd? #=> true
    4.odd? #=> false
    8.3.ceil #=> 9
    8.3.floor #=> 8
    15.next #=> 16
    15.pred #=> 14
    (-4).pred #=> -5
    15.to_s  #=> "15"
    15.gcd(5) #=> 5
    5.times do |i| print i, " " end #=> 0 1 2 3 4
  ```
  * La classe TrueClass,FalseClass et NilClass
   ```ruby
    true.class #=> TrueClass
    false.class #=> FalseClass
    nil.class #=> NilClass
   ```
  * La classe Array
  ```ruby
    [1,2,3,"aq"].class #=> Array
  ```
  Exemple des methodes:
  ```ruby
    array = ["a","b","c"] #=>["a","b","c"]
    array = %w(a b c) #=>["a","b","c"]
    array = [0, 1, 2, 3, 4]
    array.length #=> 5
    array.first  #=> 0
    array.last #=> 4
    array.take(3) #=> [0, 1, 2]
    array.drop(3) #=> [3, 4]
    array[2] #=> 2
    array[5] #=> nil
    array.pop #=> [0,1,2,3]
    array.push(99) #=> [0,1,2,3,4,99]
    array.delete(1) #=> [0, 2, 3, 4]
    array.delete_at(0) #=> [1, 2, 3, 4]
    array.reverse #=> [4, 3, 2, 1, 0]
    array.sort #=> [0,1,2,3,4]
    array.select { |number| number > 2 } #=> [3,4]
    array.join #=> "1234"
    array.join("*") #=> "1*2*3*4"
    array.each do |element|
      puts element
       end
        #=> 0
        #=> 1
        #=> 2
        #=> 3
        #=> 4

    array.map { |element| element * 2 }
      puts element
       end
        #=>  0
        #=>  2
        #=>  4
        #=>  6
        #=>  8
    array = [1, 1, 2, 2]
    array.uniq #=> [1, 2]
    array.concat([5, 6, 7], [8, 9, 10])
    #=> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
  ```
## Interpolation
  ```ruby
    name="amine"
    p "my name is #{name}" #=>my name is amine
    p 'my name is #{name}' #=>my name is \#{name}
  ```
## Les conditions
  ```ruby
    condition=true
    if(condition)
      p'hi'
    else
      p 'bye'
    end
    #==> "hi"

    unless(condition)
    p 'hi'
    else
    p 'bye'
    end
    #=> "bye"

    if(!condition)
      p'hi'
    elsif(false)
      p 'bye'
    else
      p ''
    end
    #=> ""

    condition1=true
    condition2=false
    if(condtion1==true && condtion2==false)
      p  'hi'
    end
    #=> "hi"

    if(condtion1==true || condtion2==true)
      p  'hi'
    end
    #=> "hi"
  ```
## Les boucles
  ```ruby
    i=1
    while(i<5)
    p i
    i=i+1
    end
     => 1
        2
        3
        4

    i=1
    until(i>5)
    p i
    i=i+1
    end
     => 1
        2
        3
        4

    arr=[1,2,3,4,5]
    for item in arr
    p item
    end
     => 1
        2
        3
        4
        5
  ```
## Les fonction
  ```ruby
    def my_method (param1, param2)
    param1 + param2
    end
  ```
  * Exemple
  ```ruby
     def nbpremier(nb)
       flag=false
          for i in (2..nb/2)
            if (nb % i == 0)
               flag=true
            end
          end
          if(flag==false)
             p "le nbr est premier"
          else
             p "le nbr n'est pas premier"
          end
     end
     #=>[1,5,7]

