Album.all.length # => 347
Track.find_by(title: "White Room").artist # => "Eric Clapton"
Track.find_by(duration: 188133).title # => "Perfect"
Album.find_by(title: "Use Your Illusion II").artist # => "Guns N Roses"

Album.where(artist: "AC/DC").length # => 2
Track.where(duration: 158589) # => 0

Track.where(artist: "AC/DC").each {|i| puts i }

7.920000000000001

2.5.1 :045 > total = 0
 => 0 
2.5.1 :046 > Track.where(artist: "Deep Purple").each do |i|
2.5.1 :047 >     total += i.price
2.5.1 :048?>   end

2.5.1 :051 > Track.where(artist: "Eric Clapton").each do |i|
2.5.1 :052 >     tra = i
2.5.1 :053?>   tra.artist = "Britney Spears"
2.5.1 :054?>   end