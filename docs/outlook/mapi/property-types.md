---
title: Types de propriété
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fd0f25f20c9e628a80d27f2b70e01dacc98229b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786955"
---
# <a name="property-types"></a>Types de propriété

  
  
**S’applique à**: Outlook 
  
MAPI prend en charge les propriétés de valeur unique et de plusieurs valeurs. Avec une propriété à valeur unique, il existe une valeur du type de base pour la propriété. Avec une propriété à valeurs multiples, il existe plusieurs valeurs du type de base. 
  
Les types de valeur unique et plusieurs valeurs de la propriété MAPI prend en charge sont décrits dans le tableau suivant. Pour chaque type de valeur unique qui a un type de plusieurs valeurs correspondant, le type de plusieurs valeurs apparaît entre parenthèses après le type de valeur unique.
  
|**Type de propriété**|**Valeur hexadécimale**|**Description**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indique que le type de propriété est inconnu. Ce type de propriété est réservé pour une utilisation avec les méthodes d’interface.  <br/> |
|PT_NULL  <br/> |0001  <br/> |N’indique aucune valeur de propriété. Ce type de propriété est réservé pour une utilisation avec les méthodes d’interface et est qu'identique à OLE type VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |16 bits (2 octets) entier signé. Ce type de propriété est la même que PT_SHORT (PT_MV_SHORT) et OLE type VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Signé ou non signé 32 bits (4 octets) nombre entier. Ce type de propriété est la même que PT_LONG (PT_MV_LONG) et OLE type VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32 bits (8 octets) valeur à virgule flottante. Ce type de propriété est identique à PT_R4 (PT_MV_R4) et le type OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64 bits (8 octets) valeur à virgule flottante. Ce type de propriété est identique à PT_R8 et les types OLE VT_R8 et VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |entier de 64 bits (8 octets) interprétée comme séparateur décimal. Ce type de propriété est compatible avec le type de Microsoft Visual Basic devise et est qu'identique à OLE tapez VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valeur de type double qui est interprétée comme date et heure. La partie entière correspond à la date et la partie fractionnaire est à la fois. Ce type de propriété est la même que le type OLE VT_DATE et est compatible avec la représentation du temps Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000 A  <br/> |Valeur SCODE ; entier non signé de 32 bits (4 octets). Ce type de propriété est le même que le type OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |PAGE 000C  <br/> |16 bits (2 octets) valeur booléenne où zéro est égale à **true** et **la valeur true**est égal à zéro. Ce type de propriété est le même que le type OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |D 000  <br/> |Pointeur vers un objet qui implémente l’interface **IUnknown** . Ce type de propriété est similaire à plusieurs types OLE comme VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Signé ou non signé 64 bits (8 octets) nombre entier qui utilise la structure **LARGE_INTEGER** . Ce type de propriété est la même que PT_I8 et OLE type VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Chaîne de caractère nul 8 bits (2 octets) caractères. Ce type de propriété est le même que le type OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Chaîne de caractère nul 16 bits (2 octets) caractères. Propriétés avec ce type ont le type de propriété réinitialiser pour PT_UNICODE lors de la compilation par le symbole UNICODE et PT_STRING8 lors de la ne compilation pas par le symbole UNICODE. Ce type de propriété est la même que le type OLE VT_LPSTR pour les propriétés qui en résulte PT_STRING8 et VT_LPWSTR des propriétés PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64 bits (8 octets) et l’heure entier sous la forme d’une structure **FILETIME** . Ce type de propriété est le même que le type OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valeur de la structure **CLSID** . Ce type de propriété est le même que le type OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Taille de la variable, 16 bits (2 octets) **COUNT** suivie d’une structure.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Taille de la variable, un tableau d’octets représentant une ou plusieurs des structures de Restriction.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Taille de la variable, 16 bits (2 octets) **nombre** d’actions (pas des octets) suivie de celle nombreuses structures d’Action de la règle.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valeur de structure **SBinary** , un tableau d’octets comptés.  <br/> |
   
> [!NOTE]
> Pour déterminer la valeur Hex pour le type de propriété à valeurs multiples, ou la PT_MV indicateur (0 x 00001000) à la valeur hexadécimale pour la propriété type. Par exemple, la valeur Hex pour PT_MV_UNICODE est 0x101F et la valeur Hex pour PT_MV_BINARY est 0 x 1102. 
  

