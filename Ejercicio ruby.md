def to_camel_case(text)
  words = text.split(/[-_]/)  # aca se supone que dividiria en texto
  result = words.map.with_index do |word, index|
    if index == 0
      word
    else
      word.capitalize  # la primera letra se convertira en mayuscula
    end
  end
  result[0] = result[0].downcase if result[0] != result[0].upcase  # primera palabras a minisculas
  result.join(' ')  # 
end

# Ejemplos de uso:
puts to_camel_case("the-stealth-warrior")      # "the Stealth Warrior"
puts to_camel_case("The_Stealth_Warrior")      # "The_Stealth_Warrior"
puts to_camel_case("The_Stealth-Warrior")      # "The_Stealth-Warrior"
