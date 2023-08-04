-- Ссылка на Библиотеку
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Robojini/Tuturial_UI_Library/main/UI_Template_1"))()
--[[ 
В данный момент стоит тема "RJTheme3" ,
вы можете использовать другую тему приведённую ниже -
"RJTheme1"
"RJTheme2"
"RJTheme3"
"RJTheme4"
"RJTheme5"
"RJTheme6"
"RJTheme7"
"RJTheme8"
//////////////////////////////////////////////////////////////////

Что бы сделать свою тему , уберите часть скрипта из "комминтариев" ,
который находится чуть ниже , и вместо "RJTheme3" в переменной "Windows" - 
напишите переменную которая используется в скрипте чуть ниже .
]]
--[[
local colors = {
	-- Цвет фона у Секций
    SchemeColor = Color3.fromRGB(150, 72, 148),
	-- Цвет фона в правой части UI
	Background = Color3.fromRGB(15,15,15),
	-- Цвет фона в левой части UI
    Header = Color3.fromRGB(15,15,15),
	-- Цвет текста
    TextColor = Color3.fromRGB(255,255,255),
	-- Цвет фона у кнопок
    ElementColor = Color3.fromRGB(20, 20, 20)
}
]]


local Window = Library.CreateLib("KanavaScript by XJle6220923", "RJTheme3")

local Tab = Window:NewTab("Главное")

local Section = Tab:NewSection("Главное снизу!")


Section:NewButton("Анти-река", "Удаляет крч триггеры смерти, и подскальзывания", function()
    game.Workspace.RagdollParts:Destroy()
    game.Workspace.KillParts:Destroy()
end)

Section:NewButton("Анти-канава-килл", "Не даёт умереть в канаве", function()
    game.Workspace.startPart:Destroy()
    game.Workspace.Kil:Destroy()
end)

Section:NewButton("Анти-костёр", "Удаляет крч триггер", function()
    game.Workspace.FireParts:Destroy()
end)

Section:NewToggle("Скорость", "Скорость", function(state)
    if state then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 75
    else
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
    end
end)

Section:NewSlider("Своя скорость", "Кастомная скорость", 500, 16, function(s) -- 500 (Макс. значение) | 0 (Мин. значение)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

Section:NewToggle("Noclip+AntiFling", "By XJle6220923", function(state)
    if state then
        local player = game.Players.LocalPlayer.Character
player.Torso.CanCollide = false
player.Head.CanCollide = false
    else
        local player = game.Players.LocalPlayer.Character
player.Torso.CanCollide = true
player.Head.CanCollide = true
    end
end)

Section:NewSlider("Высота шага", "А чё тут объяснять", 500, 0, function(s) -- 500 (Макс. значение) | 0 (Мин. значение)
    game.Players.LocalPlayer.Character.Humanoid.HipHeight = s
end)


local Tab = Window:NewTab("Веселье")

local Section = Tab:NewSection("Веселье")


Section:NewButton("Удалить деревья", "Удаляет деревья", function()
    game.Workspace.Trees:Destroy()
end)

Section:NewButton("Включить свою эмоцию", "Включить свою эмоцию, ну бля", function()
    game:GetService("ReplicatedStorage").Remotes.Emote:FireServer()
end)

Section:NewButton("Откидывание/FlingGUI", "Откидывалка!", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/0Ben1/fe./main/Fling%20GUI"))()
end)

Section:NewToggle("Фейковое зависание/FakeLaag", "Почти на все игры!", function(state)
    if state then
        local player = game.Players.LocalPlayer.Character
player.HumanoidRootPart.Anchored = true
    else
        local player = game.Players.LocalPlayer.Character
player.HumanoidRootPart.Anchored = false
    end
end)

Section:NewButton("Опьянеть...", "Хе-хе-хе", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/Username11231/Username11231/main/README.md'))()
end)

local Tab = Window:NewTab("Телепортации")

local Section = Tab:NewSection("Всё телепортации!")

Section:NewButton("Телепортация к игрокам(GUI)", "XD", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/AbDM2er1"))()
end)

Section:NewButton("Крыша дома", "Null", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-230.917465, 2100.49878, 198.908508, 0.0226848181, 1.04653441e-08, -0.999742687, 1.28491422e-08, 1, 1.07595941e-08, 0.999742687, -1.30899149e-08, 0.0226848181)
end)

Section:NewButton("Крыша гаража", "Null", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(87.383728, 2071.49951, 24.7613411, -0.0666142404, -4.14379286e-08, 0.997778833, 1.14683509e-07, 1, 4.91867347e-08, -0.997778833, 1.17705312e-07, -0.0666142404)
end)

Section:NewButton("Под карту(Для отхила)", "Null", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-21.6261234, -10236.9316, -71.4428253, 0.169004753, 0.141610011, -0.975389123, -3.63696656e-10, 0.989624679, 0.143676758, 0.985615253, -0.024282055, 0.167251274)
end)

Section:NewButton("В секретку", "Null", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-214.039612, 2061.49976, 224.547104, -0.998698115, 0, -0.0510110706, 0, 1, 0, 0.0510110706, 0, -0.998698115)
end)
