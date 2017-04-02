# a-good-use-of-defined-and-memoization



class Person
  attr_accessor :first_name, :last_name
  

 
  def full_name
  	
    return @full_name if defined?(@full_name) # first time "defined?(@full_name)"" is nil but afterthat first time it through values 
    
    @full_name = "#{first_name}#{last_name}"
  end
end

@test = Person.new()
@test.first_name = "ABC"
@test.last_name = "CDE"
p @test.full_name
@test.first_name = "XABC"
@test.last_name = "XDEF"
p @test.full_name



output :
"ABCCDE"
"ABCCDE"

