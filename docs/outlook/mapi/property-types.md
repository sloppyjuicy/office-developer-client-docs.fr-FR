---
title: Types de propriétés
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328489"
---
# <a name="property-types"></a>Types de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI prend en charge à la fois les propriétés à valeur unique et à valeurs multiples. Avec une propriété à valeur unique, il existe une valeur du type de base pour la propriété. Avec une propriété à valeurs multiples, il existe plusieurs valeurs du type de base. 
  
Les types de propriété à valeur unique et à valeurs multiples pris en charge par MAPI sont décrits dans le tableau suivant. Pour chaque type à valeur unique qui a un type à plusieurs valeurs correspondant, le type à valeurs multiples apparaît entre parenthèses après le type à valeur unique.
  
|**Type de propriété**|**Valeur hex**|**Description**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indique que le type de propriété est inconnu. Ce type de propriété est réservé à une utilisation avec des méthodes d'interface.  <br/> |
|PT_NULL  <br/> |0,001  <br/> |Indique qu'aucune valeur de propriété n'est ajoutée. Ce type de propriété est réservé à une utilisation avec les méthodes d'interface et est identique au type OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0,002  <br/> |Entier 16 bits (2 octets) signé. Ce type de propriété est identique à PT_SHORT (PT_MV_SHORT) et au type OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |pagin  <br/> |Entier signé ou non signé 32 bits (4 octets). Ce type de propriété est identique à PT_LONG (PT_MV_LONG) et au type OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |valeur à virgule flottante 32 bits (8 octets). Ce type de propriété est identique à PT_R4 (PT_MV_R4) et au type OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0,005  <br/> |valeur à virgule flottante 64 bits (8 octets). Ce type de propriété est identique à PT_R8 et aux types OLE VT_R8 et VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |entier 64 bits (8 octets) interprété comme un nombre décimal. Ce type de propriété est compatible avec le type monétaire Microsoft Visual Basic et est identique au type OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valeur de type double qui est interprétée comme une date et une heure. Le composant entier est la date et la fraction le temps. Ce type de propriété est identique au type de propriété VT_DATE OLE et est compatible avec la représentation temporelle Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valeur SCODE; entier non signé 32 bits (4 octets). Ce type de propriété est identique au type OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |valeur booléenne 16 bits (2 octets) où zéro est égal à **false** et différent de zéro égal à **true**. Ce type de propriété est identique au type OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Pointeur vers un objet qui implémente l'interface **IUnknown** . Ce type de propriété est similaire à plusieurs types OLE tels que VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entier 64 bits signé ou non signé (8 octets) qui utilise la structure **LARGE_INTEGER** . Ce type de propriété est identique à PT_I8 et au type OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Chaîne de caractères 8 bits (2 octets) terminée par un caractère null. Ce type de propriété est identique au type OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Chaîne de caractères 16 bits (2 octets) terminée par un caractère null. Les propriétés de ce type ont le type de propriété Reset à PT_UNICODE lors de la compilation avec le symbole UNICODE et PT_STRING8 en l'absence de compilation avec le symbole UNICODE. Ce type de propriété est identique au type OLE VT_LPSTR pour les propriétés PT_STRING8 et VT_LPWSTR pour les propriétés PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |valeur entière de données de 64 bits (8 octets) et de temps sous la forme d'une structure **fileTime** . Ce type de propriété est identique au type OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valeur de la structure **CLSID** . Ce type de propriété est identique au type OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Taille de la variable, **nombre** de 16 bits (2 octets) suivi d'une structure.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Taille de la variable, tableau d'octets représentant une ou plusieurs structures de restriction.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Taille de la variable, **nombre** de 16 bits (2 octets) des actions (et non des octets) suivis de nombreuses structures d'action de règle.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valeur de structure **SBinary** , un tableau d'octets compté.  <br/> |
   
> [!NOTE]
> Pour déterminer la valeur hexadécimale du type de propriété à valeurs multiples ou l'indicateur PT_MV (0x00001000) à la valeur hexadécimale pour le type de propriété. Par exemple, la valeur hexadécimale pour PT_MV_UNICODE est 0x101F et la valeur hexadécimale pour PT_MV_BINARY est 0x1102. 
  

