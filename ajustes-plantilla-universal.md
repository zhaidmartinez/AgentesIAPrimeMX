# Ajustes Requeridos para Alineación con Plantilla Universal Xami-CX_V1

## 1. Estructura de Arquitectura - Agregar Bloque B Completo

### Para TODOS los agentes colaboradores:
```yaml
# B · Rol & Alcance
role: "Especialista en análisis comercial y métricas de ventas para Prime MX"
authority_level: "partial"  # full | partial | none
allowed_actions: [
  "generar_consultas_sql_ventas",
  "interpretar_metricas_comerciales", 
  "proporcionar_insights_accionables",
  "invocar_power_up_athena"
]
```

### Para el Orchestrator:
```yaml
# B · Rol & Alcance  
role: "Coordinador central para routing inteligente de consultas de business intelligence"
authority_level: "full"
allowed_actions: [
  "clasificar_intenciones",
  "enrutar_consultas",
  "inyectar_contexto",
  "coordinar_respuestas_multi_dominio"
]
```

## 2. Protocolo de Colaboración Mejorado

### Para agentes colaboradores:
```yaml
# C · Protocolo de Colaboración
handshake: "sessionAttributes JSON con user_role, region, clave_unica, period_context"
routing_logic: "LLM-router"
timeout_ms: 6000
fallback: "Derivar consulta a Prime-Strategic-Intelligence para análisis cross-domain"
```

## 3. Herencia de Bloques Explícita

### Para el Orchestrator agregar:
```yaml
# E · Herencia de bloques
inherit_blocks: ["Base de Conocimiento", "Guard-rails", "Manejo de PII"]
```

### Para colaboradores mantener:
```yaml
inherit_blocks: ["Base de Conocimiento", "Guard-rails", "Manejo de PII"]
```

## 4. Completar Manejo de PII

### Agregar a TODOS los agentes que no lo tengan:
```yaml
# 8 · Manejo de PII
consent_phrase: "Para generar este análisis necesito confirmar tu nivel de acceso"
email_regex: "\\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\\.[A-Za-z]{2,}\\b"
phone_regex: "\\b(?:\\+?[0-9]{1,3}[-.\s]?)?(?:\\([0-9]{1,3}\\)[-.\s]?)?[0-9]{1,4}[-.\s]?[0-9]{1,4}[-.\s]?[0-9]{1,9}\\b"
pii_destination: "prime_[agente]_audit_log"
```

## 5. Estandarizar Variables & Placeholders

### Formato consistente para todos:
```yaml
# 5 · Variables & Placeholders
variables: [
  {"name": "{{user_role}}", "default": "No autorizado", "description": "Nivel jerárquico del usuario"},
  {"name": "{{user_region}}", "default": "Nacional", "description": "Región asignada al usuario"},
  {"name": "{{current_period}}", "default": "Mes actual", "description": "Período de análisis"}
]
```

## 6. Mejorar Checklist de Despliegue

### Agregar ítems faltantes:
```yaml
# 12 · Checklist de Despliegue
deployment_checklist: [
  "✅ Plantilla Universal Xami-CX_V1 validada",
  "✅ Herencia de bloques configurada correctamente",
  "✅ Protocolo de colaboración probado con supervisor",
  "✅ Variables y placeholders validados",
  "✅ Manejo de PII completo y probado",
  "✅ Guard-rails de seguridad validados",
  "✅ Ejemplos adversariales probados",
  "✅ Agente Validador (modelo o3) ejecutado exitosamente"
]
```

## 7. Observabilidad Mejorada

### Agregar métricas de conformidad:
```yaml
# 13 · Observabilidad & KPIs
log_events: [..., "template_compliance_check", "inheritance_validation"]
metrics_targets: {
  ...,
  "template_compliance_score": "> 95%",
  "inheritance_success_rate": "100%"
}
```

## Prioridad de Implementación:

1. **CRÍTICO**: Completar Bloque B (Rol & Alcance) en todos los agentes
2. **ALTO**: Estandarizar manejo de PII con regex patterns
3. **MEDIO**: Mejorar protocolo de colaboración
4. **BAJO**: Actualizar checklist y observabilidad

## Validación Final:
- Ejecutar Agente Validador (modelo o3) después de cada ajuste
- Verificar herencia correcta entre supervisor y colaboradores
- Probar routing y fallbacks actualizados