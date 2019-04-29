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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433527"
---
# <a name="spropvalue"></a>SPropValue

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
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
  
> Balise de propriété de la propriété. Les balises de propriété sont des entiers non signés 32 bits constitués de l'identificateur unique de la propriété dans l'ordre décroissant de 16 bits et le type de la propriété dans le bas de 16 bits.
    
 **dwAlignPad**
  
> Réservé pour MAPI; ne pas utiliser. 
    
 **Valeur**
  
> Union de valeurs de données, la valeur spécifique déterminée par le type de propriété. Le tableau suivant répertorie pour chaque type de propriété, le membre de l'Union à utiliser et le type de données associé.
    
|**Type de propriété**|**Valeur**|**Type de données de la valeur**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG (signé)  <br/> |**l** <br/> |PLUS  <br/> |
|PT_I4 ou PT_LONG (non signé)  <br/> |**suffix** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**flt** <br/> |flottant  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**clic** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |entier court non signé  <br/> |
|PT_CURRENCY  <br/> |**Tabs** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**Regardez** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**pied** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**plateau** <br/> |BYTE [array]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 ou PT_LONGLONG  <br/> |**&** <br/> |**LARGE_INTEGER** <br/> |
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
|PT_NULL ou PT_OBJECT  <br/> |**x** <br/> |PLUS  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |RÉSIDUEL\*  <br/> |
   
## <a name="remarks"></a>Remarques

Le membre **ulPropTag** est composé de deux parties: 
  
- Identificateur dans l'ordre décroissant de 16 bits.
    
- Un type dans les bits de poids faible 16.
    
L'identificateur est une valeur numérique comprise dans une plage particulière. MAPI définit des plages d'identificateurs pour décrire ce à quoi la propriété est utilisée et qui est responsable de sa maintenance. MAPI définit des contraintes pour chacune des balises de propriété qu'il prend en charge dans le fichier d'en-tête Mapitags. h.
  
Le type indique le format de la valeur de la propriété. MAPI définit des constantes pour chaque type de propriété qu'il prend en charge dans le fichier d'en-tête Mapidefs. h. 
  
Pour obtenir la liste complète des plages de propriétés valides pour les identificateurs et les types de propriétés, voir l'annexe relative aux [identificateurs et aux types](property-identifiers-and-types.md) de propriétés. 
  
Le membre **dwAlignPad** est utilisé comme remplissage pour garantir un alignement correct sur les ordinateurs qui nécessitent un alignement sur 8 octets pour les valeurs 8 octets. Les développeurs qui écrivent du code sur ces ordinateurs doivent utiliser des routines d'allocation de mémoire qui allouent les tableaux **SPropValue** sur des limites de 8 octets. 
  
Pour plus d'informations, reportez-vous à la rubrique [MAPI Property type Overview](mapi-property-type-overview.md) et [mise à jour des propriétés MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

