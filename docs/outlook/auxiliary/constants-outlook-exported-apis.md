---
title: Constantes (Outlook des API exportées)
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Définitions constantes pour les API qui Outlook exportations.
ms.openlocfilehash: a93cb5a56cab036cf0d3c001bb91a98f88a63f82
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66084087"
---
# <a name="constants-outlook-exported-apis"></a>Constantes (Outlook des API exportées)

Cette rubrique contient des définitions constantes pour les API qui Outlook exportations.
  
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
|PCAFSIF_MSGEID_IS_SEARCH_KEY |0x00000001 |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Identificateurs de répartition divers

Outlook expose les identificateurs de distribution suivants (dispids) afin que les développeurs puissent utiliser [IDispatch::Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) pour accéder à la propriété ou à la méthode correspondante, ou écouter l’événement correspondant.
  
|**Constante associée**|**Valeur dispidée**|**Description**|**Interface applicable**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** | 0xF024 |Utilisé pour appeler la propriété correspondante sur un élément pour vérifier si l’élément a été modifié mais n’a pas été enregistré. |Objets au niveau de l’élément |
|**dispidShowSenderPhoto** | 0xF0D0 |Utilisé pour appeler la méthode correspondante sur l’explorateur ou l’inspecteur pour spécifier s’il faut afficher l’image d’un contact, en fonction d’un argument donné. |Explorateur ou inspecteur |
|**dispidBeforePrint** | 0xFC8E |Utilisé pour gérer l’événement à partir de la fonction **IDispatch::Invoke** qui se déclenche avant une opération d’impression. |Application |
|**dispidEventReadComplete** | 0xFC8F |Utilisé pour gérer l’événement à partir de la fonction **IDispatch::Invoke qui se** déclenche lorsque Outlook a terminé la lecture des propriétés de l’élément. |Objets au niveau de l’élément |
   
## <a name="see-also"></a>Voir aussi

- [API exportées Outlook](outlook-exported-apis.md)
- [À propos des API exportées par Outlook](about-apis-exported-by-outlook.md)
- [Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Spécifier si vous souhaitez afficher l'image d'un contact dans Outlook (référence auxiliaire d'Outlook)](/previous-versions/office/gg262879(v=office.15))
- [Événements disponibles et leur DISPID (Outlook des API exportées)](available-events-and-their-dispids-outlook-exported-apis.md)
