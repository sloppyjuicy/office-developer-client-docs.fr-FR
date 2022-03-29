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
ms.openlocfilehash: 3506247641161bb0c0e42db62e314c5fab565981
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454683"
---
# <a name="spropvalue"></a>SPropValue

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété MAPI.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
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
  
> Balise de propriété de la propriété. Les balises de propriété sont des nombres droits non signés 32 bits constitués de l’identificateur unique de la propriété dans l’ordre élevé de 16 bits et du type de la propriété dans l’ordre faible de 16 bits.
    
 **dwAlignPad**
  
> Réservé à MAPI ; ne pas utiliser. 
    
 **Valeur**
  
> Union des valeurs de données, valeur spécifique dictée par le type de propriété. Le tableau suivant répertorie chaque type de propriété, le membre de l’union à utiliser et son type de données associé.
    
|**Type de propriété**|**Valeur**|**Type de données de valeur**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG (signé)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 ou PT_LONG (non signé)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**flt** <br/> |float  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**at** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [tableau]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 ou PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
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
|PT_PTR  <br/> |**lpv** <br/> |VOID \*  <br/> |
   
## <a name="remarks"></a>Remarques

Le **membre ulPropTag** est composé de deux parties : 
  
- Identificateur de l’ordre élevé de 16 bits.
    
- Type de 16 bits de bas ordre.
    
L’identificateur est une valeur numérique dans une plage particulière. MAPI définit des plages pour les identificateurs afin de décrire l’utilisation de la propriété et la personne responsable de sa maintenance. MAPI définit des contraintes pour chacune des balises de propriété qu’il prend en charge dans le fichier d’en-tête Mapitags.h.
  
Le type indique le format de la valeur de la propriété. MAPI définit des constantes pour chacun des types de propriétés qu’il prend en charge dans le fichier d’en-tête Mapidefs.h. 
  
Pour obtenir la liste complète des plages de propriétés valides pour les identificateurs et les types de propriétés, voir l’annexe [Identificateurs et types de](property-identifiers-and-types.md) propriétés. 
  
Le **membre dwAlignPad** est utilisé comme remplissage pour s’assurer d’un alignement correct sur les ordinateurs qui nécessitent un alignement de 8 byte pour des valeurs de 8 byte. Les développeurs qui écrivent du code sur ces ordinateurs doivent utiliser des routines d’allocation de mémoire qui allouent les tableaux **SPropValue** aux limites de 8 byte. 
  
Pour plus d’informations, voir [Vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md) et [mise à jour des propriétés MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

