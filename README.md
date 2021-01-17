getgenv().farmer = false

local RRP2 = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local ItemFarm = Instance.new("TextButton")
local DisableItemFarm = Instance.new("TextButton")
local NameHide = Instance.new("TextButton")
local Respawn = Instance.new("TextButton")

--Properties:

RRP2.Name = "RRP2"
RRP2.Parent = game.CoreGui
RRP2.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = RRP2
Frame.BackgroundColor3 = Color3.fromRGB(85, 0, 127)
Frame.BackgroundTransparency = 0.200
Frame.BorderColor3 = Color3.fromRGB(85, 0, 255)
Frame.Position = UDim2.new(0.0127272727, 0, 0.379606873, 0)
Frame.Size = UDim2.new(0, 337, 0, 440)
Frame.Active = true
Frame.Draggable = true
Frame.Visible = true 


Title.Name = "Title"
Title.Parent = Frame
Title.BackgroundColor3 = Color3.fromRGB(46, 46, 46)
Title.BackgroundTransparency = 1.000
Title.BorderColor3 = Color3.fromRGB(85, 0, 255)
Title.Size = UDim2.new(0, 337, 0, 50)
Title.Font = Enum.Font.Bangers
Title.Text = "RRP2Mods by chad"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextSize = 40.000

ItemFarm.Name = "ItemFarm"
ItemFarm.Parent = Frame
ItemFarm.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ItemFarm.BackgroundTransparency = 1.000
ItemFarm.BorderColor3 = Color3.fromRGB(85, 255, 255)
ItemFarm.Position = UDim2.new(0.201780409, 0, 0.206818178, 0)
ItemFarm.Size = UDim2.new(0, 200, 0, 50)
ItemFarm.Font = Enum.Font.Bangers
ItemFarm.Text = "ItemFarm"
ItemFarm.TextColor3 = Color3.fromRGB(255, 255, 255)
ItemFarm.TextSize = 30.000
ItemFarm.MouseButton1Click:Connect(function()
	getgenv().farmer = true;
	while wait() and getgenv().farmer == true do 
		for i,v in pairs(Game:GetService('Workspace').DroppedItems:GetChildren()) do
			if v:IsA'Tool' then
				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame
			end
		end
	end
end
)

DisableItemFarm.Name = "DisableItemFarm"
DisableItemFarm.Parent = Frame
DisableItemFarm.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
DisableItemFarm.BackgroundTransparency = 1.000
DisableItemFarm.BorderColor3 = Color3.fromRGB(85, 255, 255)
DisableItemFarm.Position = UDim2.new(0.201780409, 0, 0.388636351, 0)
DisableItemFarm.Size = UDim2.new(0, 200, 0, 50)
DisableItemFarm.Font = Enum.Font.Bangers
DisableItemFarm.Text = "DisableItemFarm"
DisableItemFarm.TextColor3 = Color3.fromRGB(255, 255, 255)
DisableItemFarm.TextSize = 30.000
DisableItemFarm.MouseButton1Click:Connect(function()
    getgenv().farmer = false
end
)

NameHide.Name = "NameHide"
NameHide.Parent = Frame
NameHide.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
NameHide.BackgroundTransparency = 1.000
NameHide.BorderColor3 = Color3.fromRGB(85, 255, 255)
NameHide.Position = UDim2.new(0.201780409, 0, 0.593181789, 0)
NameHide.Size = UDim2.new(0, 200, 0, 50)
NameHide.Font = Enum.Font.Bangers
NameHide.Text = "NameHide"
NameHide.TextColor3 = Color3.fromRGB(255, 255, 255)
NameHide.TextSize = 30.000
NameHide.MouseButton1Click:Connect(function()
    game.Players.LocalPlayer.Character.Head.Card.Frame.Namey:Destroy()
end
)
    

Respawn.Name = "Respawn"
Respawn.Parent = Frame
Respawn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Respawn.BackgroundTransparency = 1.000
Respawn.BorderColor3 = Color3.fromRGB(85, 255, 255)
Respawn.Position = UDim2.new(0.201780409, 0, 0.809090853, 0)
Respawn.Size = UDim2.new(0, 200, 0, 50)
Respawn.Font = Enum.Font.Bangers
Respawn.Text = "Respawn"
Respawn.TextColor3 = Color3.fromRGB(255, 255, 255)
Respawn.TextSize = 30.000
