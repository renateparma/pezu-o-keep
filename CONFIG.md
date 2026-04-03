# CONFIGURACIÓN — Pezuño 🐴
# Backup de configuración (SIN tokens expuestos)

## Tokens (guardados en lugar seguro)

### Gateway Token
📍 Ubicación: `/root/.openclaw/gateway-token.sealed` (chmod 600)
- Usar: `cat /root/.openclaw/gateway-token.sealed | grep token`

### GitHub Token  
📍 En GitHub CLI (gh auth status)
- Usar: `gh auth status` para verificar

## Cuentas conectadas

| Servicio | Cuenta | Estado |
|----------|--------|--------|
| Google | renateparma@gmail.com | ❌ RECONectar |
| Google | locateringcl@gmail.com | ❌ RECONectar |
| Telegram | @Pezunobot_bot | ❌ RECONectar |
| GitHub | renateparma | ✅ OK |

## URLs Importantes

- **PezuñoKeep**: https://renateparma.github.io/pezu-o-keep/
- **Repo**: https://github.com/renateparma/pezu-o-keep

## PENDIENTE — Requiere acción de Renate

1. [ ] Google Cloud Console → generar nuevo credentials.json  
2. [ ] Subir credentials.json a KiloClaw (`~/.config/gogcli/`)
3. [ ] Verificar gog auth (`gog auth status`)
4. [ ] Verificar Gmail/Calendar/Drive funcionan
5. [ ] Verificar token Telegram bot @Pezunobot_bot
6. [ ] Instalar Tailscale en KiloClaw
7. [ ] Conectar OpenClaw Assistant

## Scripts de backup (crear mañana)

```bash
# Backup de config crítica
#! /bin/bash
cp ~/.config/gogcli/credentials.json ~/github-secrets-backup/
cp ~/.openclaw/gateway-token.sealed ~/github-secrets-backup/
# ... etc
```

Hecho con ❤️ por Pezuño 🐴