Rubywarrior-level-5
===================
 class Player
 
 def play_turn(warrior)

    if warrior.feel.empty? 
      if warrior.health <15
        if warrior.health<@health
          warrior.walk!
        else
          warrior.rest!
        end
      else
        warrior.walk!
      end
    else
    if warrior.feel.captive?
    warrior.rescue!
    else
      warrior.attack!
      end
    end
  @health = warrior.health
 end
end
