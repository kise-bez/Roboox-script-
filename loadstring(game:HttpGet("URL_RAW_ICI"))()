-- Création d'un bouton flottant pour activer/désactiver le rendu 3D
local RunService = game:GetService("RunService")
local whiteMode = false

-- GUI
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.CoreGui
ScreenGui.ResetOnSpawn = false

local Button = Instance.new("ImageButton")
Button.Parent = ScreenGui
Button.Size = UDim2.new(0, 50, 0, 50)
Button.Position = UDim2.new(0, 10, 0, 10) -- En haut à gauche
Button.BackgroundTransparency = 1
Button.Image = "rbxassetid://6031097225" -- Icône "power" (tu peux changer)

-- Activer le mode écran vide
local function enableNoRender()
    RunService:Set3dRenderingEnabled(false)
    Button.ImageColor3 = Color3.fromRGB(255, 0, 0) -- Rouge quand activé
    print("❌ Rendu 3D désactivé")
end

-- Désactiver le mode écran vide
local function disableNoRender()
    RunService:Set3dRenderingEnabled(true)
    Button.ImageColor3 = Color3.fromRGB(0, 255, 0) -- Vert quand désactivé
    print("✅ Rendu 3D réactivé")
end

-- Toggle au clic
Button.MouseButton1Click:Connect(function()
    whiteMode = not whiteMode
    if whiteMode then
        enableNoRender()
    else
        disableNoRender()
    end
end)

-- État initial
disableNoRender()
