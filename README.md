fill('hills2)

function platform(i) {
  y = i * 300
  p = stamp('platform',375,i*300,220)
  p.startY = y
}
repeat(platform, 4)

hero = stanp('plumber',385,750,300)
function touching() {
  if (x > hero.x) {
    hero.change('plumber')
  } else {
    hero.change('plumber2')
  }
  hero.move(x,y,500)
}
