---
title: Constantes (Outlook des API exportées)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Cette rubrique contient des définitions de constantes pour les API exportées par Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319872"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (Outlook des API exportées)

Cette rubrique contient des définitions de constantes pour les API exportées par Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Définitions de la prise en charge des fuseaux horaires

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Définitions de la prise en charge des catégories

|**Constante**|**Définition**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificateurs de dispatch divers

Outlook expose les identificateurs de dispatch suivants pour permettre aux développeurs d'utiliser [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) pour accéder à la propriété ou la méthode correspondante, ou écouter l'événement correspondant. 
  
|**Constante associée**|**Valeur DISPID**|**Description**|**Interface applicable**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Utilisé pour appeler la propriété correspondante sur un élément afin de vérifier si l'élément a été modifié mais n'a pas été enregistré.  <br/> |Objets au niveau élément  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Utilisé pour appeler la méthode correspondante dans l'Explorateur ou l'inspecteur afin de spécifier s'il faut afficher l'image d'un contact, en fonction d'un argument donné.  <br/> |Explorateur ou inspecteur  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Permet de gérer l'événement à partir de la fonction **IDispatch:: Invoke** qui se déclenche avant une opération d'impression.  <br/> |Application  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Permet de gérer l'événement à partir de la fonction **IDispatch:: Invoke** qui se déclenche quand Outlook a terminé de lire les propriétés de l'élément.  <br/> |Objets au niveau élément  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [API exportées Outlook](outlook-exported-apis.md)
- [À propos des API exportées par Outlook](about-apis-exported-by-outlook.md)
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Événements disponibles et leur DISPID (Outlook des API exportées)](available-events-and-their-dispids-outlook-exported-apis.md)

