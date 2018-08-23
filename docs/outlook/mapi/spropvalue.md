---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 60528162917a8a383060adbcadefb610aa42ce32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580970"
---
# <a name="spropvalue"></a>SPropValue

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une propriété MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
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
  
> Balise de propriété pour la propriété. Balises de propriété sont des entiers non signés 32 bits constituée de l’identificateur unique de la propriété dans l’ordre de haut niveau 16 bits et le type de propriété dans les 16 bits de poids faible.
    
 **dwAlignPad**
  
> Réservé pour MAPI ; n’utilisez pas. 
    
 **Valeur**
  
> Union des valeurs de données, la valeur spécifique dictée par le type de propriété. Le tableau suivant répertorie pour chaque type de propriété, le membre de l’union qui doit être utilisé et son type de données associé.
    
|**Type de propriété**|**Valeur**|**Type de données de valeur**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**J’ai** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG (connecté)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 ou PT_LONG (non signé)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**flt** <br/> |float  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**Double** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |entier court  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**à** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Corbeille** <br/> |OCTETS [array]  <br/> |
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
|PT_PTR  <br/> |**LPV** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Remarques

Le membre **ulPropTag** est composé de deux parties : 
  
- Un identificateur dans l’ordre de haut niveau 16 bits.
    
- Un type dans les 16 bits de poids faible.
    
L’identificateur est une valeur numérique dans une plage spécifique. MAPI définit les plages pour les identificateurs décrire la propriété qui est utilisée pour et qui est chargé de maintenance. MAPI définit des contraintes pour chacune des balises de propriété pris en charge dans le fichier d’en-tête Mapitags.h.
  
Le type indique le format de la valeur de propriété. MAPI définit des constantes pour chacun des types de propriété pris en charge dans le fichier d’en-tête Mapidefs.h. 
  
Pour une liste complète des plages de propriété valide pour les identificateurs et les types de propriété, voir l’annexe [les Types et les identificateurs de propriété](property-identifiers-and-types.md) . 
  
Le membre **dwAlignPad** est utilisé comme remplissage pour effectuer un alignement correct que sur les ordinateurs qui nécessitent l’alignement de 8 octets pour les valeurs de 8 octets. Développeurs, écrire du code sur ces ordinateurs doivent utiliser des routines d’allocation de mémoire qui affectent les tableaux **SPropValue** sur les limites de 8 octets. 
  
Pour plus d’informations, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md) et [Mise à jour des propriétés MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

