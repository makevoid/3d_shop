# 3D Shop

initial implementation inside 3dmaking repo: <http://github.com/makevoid/3dmaking>

see lib/3dshop/3dshop.rb in that repo


### what:

user wants to print an STL (or select one from thingiverse)

### flow:

user = User.create params[:email]

stl = user.upload_stl()
gcode = Slicer.generate stl
App.send user, gcode.cost # gcode.cost.class => Gcode::Cost
- page with spinner
- email > link to page with spinner

### good case (cost is ok)

user.pay gcode

 - payment (paypal) integration



> shipping
> returns


] Shop.slicer_configs = {...}
