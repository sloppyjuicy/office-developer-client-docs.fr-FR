---
title: Types de propriétés
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407052"
---
# <a name="property-types"></a>Types de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI prend en charge les propriétés à valeur unique et à valeurs multiples. Avec une propriété à valeur unique, il existe une valeur du type de base pour la propriété. Avec une propriété à valeurs multiples, il existe plusieurs valeurs du type de base. 
  
Les types de propriétés à valeur unique et à valeurs multiples que MAPI prend en charge sont décrits dans le tableau suivant. Pour chaque type à valeur unique correspondant à plusieurs valeurs, le type à valeurs multiples apparaît entre parenthèses après le type à valeur unique.
  
|**Type de propriété**|**Valeur hex**|**Description**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indique que le type de propriété est inconnu. Ce type de propriété est réservé à une utilisation avec des méthodes d’interface.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Indique aucune valeur de propriété. Ce type de propriété est réservé à une utilisation avec des méthodes d’interface et est identique au type OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Signed 16-bit (2-byte) integer. Ce type de propriété est identique à PT_SHORT (PT_MV_SHORT) et au type OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Unteger 32 bits (4 bits) signé ou non signé. Ce type de propriété est identique à PT_LONG (PT_MV_LONG) et au type OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |Valeur à valeur à valeur flottante 32 bits (8 bits). Ce type de propriété est identique à PT_R4 (PT_MV_R4) et au type OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |Valeur à valeur à valeur flottante de 64 bits (8 byte). Ce type de propriété est identique à PT_R8 et les types OLE VT_R8 et VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY )  <br/> |0006  <br/> |Integer 64 bits (8 byte) interprété comme décimal. Ce type de propriété est compatible avec le type MICROSOFT Visual Basic CURRENCY et est identique au type OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valeur double interprétée comme date et heure. La partie de nombres longs est la date et la partie fraction est l’heure. Ce type de propriété est identique au type OLE VT_DATE et est compatible avec la représentation Visual Basic’heure microsoft.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valeur SCODE ; Integer non signé 32 bits (4 bits). Ce type de propriété est identique au type OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |Valeur boolé générale de 16 bits (2 bits) où zéro est égal à **false** et non zéro à **true**. Ce type de propriété est identique au type OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Pointeur vers un objet qui implémente **l’interface IUnknown.** Ce type de propriété est similaire à plusieurs types OLE tels que VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entière 64 bits (8 LARGE_INTEGER) signée ou **non** signée. Ce type de propriété est le même que PT_I8 et le type OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Chaîne de caractères de 8 bits (2 caractères) terminée par null. Ce type de propriété est identique au type OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Chaîne de caractères de 16 bits (2 caractères) terminée par null. Les propriétés de ce type ont le type de propriété réinitialisé à PT_UNICODE lors de la compilation avec le symbole UNICODE et à PT_STRING8 en cas de non-compilation avec le symbole UNICODE. Ce type de propriété est identique au type OLE VT_LPSTR pour les propriétés PT_STRING8 et VT_LPWSTR pour PT_UNICODE propriétés  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |Valeur d’heure et données d’un nombre entière de 64 bits (8 bits) sous la forme d’une structure **FILETIME.** Ce type de propriété est identique au type OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valeur de structure **CLSID.** Ce type de propriété est identique au type OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Taille de la variable, nombre de 16  bits (2 byte) suivi d’une structure.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Taille variable, tableau d’byte représentant une ou plusieurs structures de restriction.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Taille variable, nombre d’actions (et non  d’octets) de 16 bits (2 octets) suivi de ce nombre de structures d’action de règle.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valeur de structure **SBinary,** tableau d’byte compté.  <br/> |
   
> [!NOTE]
> Pour déterminer la valeur Hex pour le type de propriété à valeurs multiples, OU l’indicateur PT_MV (0x00001000) à la valeur Hex pour le type de propriété. Par exemple, la valeur Hex pour PT_MV_UNICODE est 0x101F et la valeur Hex pour PT_MV_BINARY est 0x1102. 
  

