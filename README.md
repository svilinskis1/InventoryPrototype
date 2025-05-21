# Basic Inventory and Dialog system - Unreal Engine
## Samera Vilinskis

### Features (and how to test):
- Inventory items in the world that can be picked up by pressing E while nearby.
- Inventory screen that holds 4 items and contains a viewport. Use ESC to open and close the inventory, or click the close button. 
- Items can be rotated in the viewport using the mouse to click and drag, and the scroll wheel to zoom.
- 2D items can be removed from the inventory with the "forget note" button. 
- Characters that can be spoken to by pressing E while nearby.
- When spoken to multiple times, they will have different dialog. 

### Design Decisions
#### Items
The Item blueprint contains the basic functionality for all items. The placeholder 2D and 3D items inherit from this item. Currently, the mesh of the item is hardcoded - in the future, the mesh should be changed to be instance editable. When you get close to an item, a widget appears showing the required input to pick it up. This gives a visual for how close the player must be to pick it up, and helps players remember the controls. 

#### Inventory
The inventory is opened by pressing ESC. When you pick up items, they appear in your inventory, with a maximun of 4. You can drag items onto the viewport to view them in 3D. You can rotate the item by clicking and dragging, which tends to be intuitive. A zoom feature was also implemented using the mouse wheel, which helps to inspect items in closer detail.

#### Dialog system 
Interacting with dialog actors uses the same system as inventory items. When you talk to them, the game pauses until you finish their dialog. When talking to dialog actors again, they'll have something different to say - this helps to add interest to the world. 
