---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: Décrit une propriété MAPI pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 3afb98746afb74f35dec032b8c4f2c1d87a3ec68
ms.sourcegitcommit: 40d4e0c1322eed1d56edd5d869ff3d2793f27593
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2022
ms.locfileid: "66984090"
---
# <a name="spropvalue"></a>SPropValue

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété MAPI.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md)[, PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> Balise de propriété pour la propriété. Les balises de propriété sont des entiers non signés 32 bits constitués de l’identificateur unique de la propriété dans l’ordre élevé 16 bits et du type de la propriété dans les 16 bits de faible ordre.
    
 **dwAlignPad**
  
> Réservé à MAPI; n’utilisez pas. 
    
 **Valeur**
  
> Union des valeurs de données, valeur spécifique dictée par le type de propriété. Le tableau suivant répertorie chaque type de propriété, le membre de l’union à utiliser et son type de données associé.
    
|**Type de propriété**|**Valeur**|**Type de données de valeur**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**Je** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG  <br/> |**l** <br/> |LONG  <br/> |
|-  <br/> |**Ul** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**Flt** <br/> |float  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**Dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**B** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**À** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**Ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Bin** <br/> |BYTE [tableau]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 ou PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**Mvi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL ou PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR ou PT_FILE_HANDLE  <br/> |**Lpv** <br/> |VIDE \*  <br/> |
   
## <a name="remarks"></a>Remarques

Le membre **ulPropTag** est constitué de deux parties : 
  
- Identificateur dans l’ordre supérieur de 16 bits.
    
- Type dans l’ordre inférieur de 16 bits.
    
L’identificateur est une valeur numérique dans une plage particulière. MAPI définit des plages pour les identificateurs afin de décrire à quoi la propriété est utilisée et qui est responsable de sa maintenance. MAPI définit des contraintes pour chacune des balises de propriété qu’il prend en charge dans le fichier d’en-tête Mapitags.h.
  
Le type indique le format de la valeur de la propriété. MAPI définit des constantes pour chacun des types de propriétés qu’il prend en charge dans le fichier d’en-tête Mapidefs.h. 
  
Pour obtenir la liste complète des plages de propriétés valides pour les identificateurs et les types de propriétés, consultez l’annexe [Identificateurs et types de propriétés](property-identifiers-and-types.md) . 
  
Le membre **dwAlignPad** est utilisé comme remplissage pour garantir un alignement correct sur les ordinateurs qui nécessitent un alignement de 8 octets pour les valeurs de 8 octets. Les développeurs qui écrivent du code sur ces ordinateurs doivent utiliser des routines d’allocation de mémoire qui allouent les tableaux **SPropValue** sur des limites de 8 octets. 

Le ``SPropValue::ul`` membre n’a pas de type de propriété MAPI correspondant, car le VT_UI4 d’OLE n’est pas mappé à MAPI. Pour plus d’informations, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md) et [mise à jour des propriétés MAPI](updating-mapi-properties.md).
Lorsque le type de propriété d’un SPropValue indique PT_LONG, le membre actif de l’union UPV est généralement ``l``et l’accès ``ul`` constitue un comportement non défini conformément à la norme C. 

## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

