---
title: Constantes (Outlook des API exportées)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Cette rubrique contient des définitions de constantes pour les API qui exporte Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386074"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (Outlook des API exportées)

Cette rubrique contient des définitions de constantes pour les API qui exporte Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Prise en charge des définitions de fuseau horaire

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Prise en charge des définitions de catégorie

|**Constante**|**Définition**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificateurs de répartition divers

Outlook expose les identificateurs de répartition suivants (DISPID) afin que les développeurs peuvent utiliser [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) pour accéder à la propriété correspondante ou la méthode, ou écouter l’événement correspondant. 
  
|**Constante associée**|**Valeur DISPID**|**Description**|**Interface applicable**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Utilisé pour appeler la propriété correspondante sur un élément pour vérifier si l’élément a été modifié mais n’a pas été enregistré.  <br/> |Objets de niveau élément  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Utilisé pour appeler la méthode correspondante dans l’Explorateur de solutions ou l’inspecteur pour spécifier s’il faut afficher l’image d’un contact, basé sur un argument donné.  <br/> |Objet Explorer ou inspector  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Permet de gérer l’événement à partir de la fonction **IDispatch::Invoke** qui se déclenche avant une opération d’impression.  <br/> |Application  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Permet de gérer l’événement à partir de la fonction **IDispatch::Invoke** qui se déclenche quand Outlook est terminée, les propriétés de l’élément de lecture.  <br/> |Objets de niveau élément  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [API exportées Outlook](outlook-exported-apis.md)
- [À propos des API exportées par Outlook](about-apis-exported-by-outlook.md)
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Événements disponibles et leur DISPID (Outlook des API exportées)](available-events-and-their-dispids-outlook-exported-apis.md)

