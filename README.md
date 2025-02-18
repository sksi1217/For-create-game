# For-create-game
```
public void UpdateWeaponRotation(MouseState mouseState)
{
    int mouseX = mouseState.X - (Setting.WidthWindow / 2);
    int mouseY = mouseState.Y - (Setting.HeightWindow / 2);

    if (mouseX == 0 && mouseY == 0)
    {
        rotationWeapon = 0f;
        originWeapon = new Vector2(0, 16);
        if (flipEffectWeapon)
        {
            weaponSpriteEffect = SpriteEffects.None;
        }

        return;
    }

    rotationWeapon = (float)Math.Atan2(mouseY, mouseX);

    if (mouseX < 0)
    {
        rotationWeapon -= WeaponRotationOffset;
        originWeapon = new Vector2(0, 0);
        weaponSpriteEffect = SpriteEffects.FlipVertically;
    }
    else
    {
        rotationWeapon += WeaponRotationOffset;
        originWeapon = new Vector2(0, 16);
        weaponSpriteEffect = SpriteEffects.None;
    }
}
```
