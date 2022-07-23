---
title: Types de propriétés
description: Décrit les types de propriétés à valeur unique et à valeurs multiples pris en charge par MAPI dans une table présentant le type de propriété, la valeur hexadécimale et une brève description.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
ms.openlocfilehash: 4ff785ab8f08504265cb018b4e8c4a861b3223fe
ms.sourcegitcommit: 40d4e0c1322eed1d56edd5d869ff3d2793f27593
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2022
ms.locfileid: "66984084"
---
# <a name="property-types"></a>Types de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI prend en charge les propriétés à valeur unique et à valeurs multiples. Avec une propriété à valeur unique, il existe une valeur du type de base pour la propriété. Avec une propriété à valeurs multiples, il existe plusieurs valeurs du type de base. 
  
Les types de propriétés à valeur unique et à valeur multiple pris en charge par MAPI sont décrits dans le tableau suivant. Pour chaque type à valeur unique qui a un type à valeurs multiples correspondant, le type à valeurs multiples apparaît entre parenthèses après le type à valeur unique.
  
|**Type de propriété**|**Valeur hex**|**Description**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indique que le type de propriété est inconnu. Ce type de propriété est réservé pour une utilisation avec des méthodes d’interface. |
|PT_NULL  <br/> |0001  <br/> |Indique aucune valeur de propriété. Ce type de propriété est réservé pour une utilisation avec des méthodes d’interface et est identique au type OLE VT_NULL. |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Entier 16 bits (2 octets) signé. Ce type de propriété est identique à PT_SHORT (PT_MV_SHORT) et au type OLE VT_I2. |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Entier signé 32 bits (4 octets). Ce type de propriété est identique à PT_LONG (PT_MV_LONG) et au type OLE VT_I4. |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |Valeur à virgule flottante 32 bits (8 octets). Ce type de propriété est identique à PT_R4 (PT_MV_R4) et au type OLE VT_R4. |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |Valeur à virgule flottante 64 bits (8 octets). Ce type de propriété est identique à PT_R8 et les types OLE VT_R8 et VT_DOUBLE. |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |Entier 64 bits (8 octets) interprété comme décimal. Ce type de propriété est compatible avec le type MICROSOFT Visual Basic CURRENCY et est identique au type OLE VT_CY. |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valeur double interprétée comme date et heure. La partie entière est la date et la partie fraction est l’heure. Ce type de propriété est identique au type OLE VT_DATE et est compatible avec la représentation temporelle Microsoft Visual Basic. |
|PT_ERROR  <br/> |000A  <br/> |Valeur SCODE ; Entier non signé 32 bits (4 octets). Ce type de propriété est identique au type OLE VT_ERROR. |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |Valeur booléenne 16 bits (2 octets) où zéro est **égal à false** et non-zéro à **true**. Ce type de propriété est identique au type OLE VT_BOOL. |
|PT_OBJECT  <br/> |000D  <br/> |Pointeur vers un objet qui implémente l’interface **IUnknown** . Ce type de propriété est similaire à plusieurs types OLE tels que VT_UNKNOWN. |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Entier signé 64 bits (8 octets) qui utilise la structure **LARGE_INTEGER** . Ce type de propriété est identique à PT_I8 et au type OLE VT_I8. |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Chaîne de caractères de 8 bits (2 octets) terminée par une valeur Null. Ce type de propriété est identique au type OLE VT_LPSTR. |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Chaîne de caractères 16 bits (2 octets) terminée par null. Les propriétés de ce type ont le type de propriété réinitialisé à PT_UNICODE lors de la compilation avec le symbole UNICODE et à PT_STRING8 lorsqu’elles ne sont pas compilées avec le symbole UNICODE. Ce type de propriété est le même que le type OLE VT_LPSTR pour les propriétés PT_STRING8 résultantes et VT_LPWSTR pour les propriétés PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |Données entières 64 bits (8 octets) et valeur de temps sous la forme d’une structure **FILETIME** . Ce type de propriété est identique au type OLE VT_FILETIME. |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valeur de structure **CLSID**. Ce type de propriété est identique au type OLE VT_CLSID. |
|PT_SVREID  <br/> |00FB  <br/> |Taille de variable, nombre de 16 bits (2 octets **) suivi** d’une structure. |
|PT_SRESTRICT  <br/> |00FD  <br/> |Taille de variable, tableau d’octets représentant une ou plusieurs structures de restriction. |
|PT_ACTIONS  <br/> |00FE  <br/> |Taille de variable, **nombre d’actions** 16 bits (2 octets) (et non d’octets) suivi de nombreuses structures d’action de règle. |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**Valeur de structure SBinary** , tableau d’octets comptés. |
   
> [!NOTE]
> Pour déterminer la valeur Hex pour le type de propriété à valeurs multiples, OU l’indicateur PT_MV (0x00001000) à la valeur Hex pour le type de propriété. Par exemple, la valeur Hex pour PT_MV_UNICODE est 0x101F et la valeur Hex pour PT_MV_BINARY est 0x1102. 
  
MAPI partage les numéros de type valeur avec [[variantes OLE]](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-oaut/3fe7db9f-5803-4dc4-9d14-5425d3f5461f). Toutefois, tous les types OLE ne sont pas spécifiés pour MAPI. En particulier, les types non signés tels que VT_UI4 n’ont pas d’équivalent dans MAPI. La comparaison des valeurs de propriétés PT_I2/I4/I8, par exemple lors de l’évaluation de [[restrictions]](https://docs.microsoft.com/en-us/office/client-developer/outlook/mapi/spropertyrestriction) (filtres), est effectuée en tant que comparaison signée. 
