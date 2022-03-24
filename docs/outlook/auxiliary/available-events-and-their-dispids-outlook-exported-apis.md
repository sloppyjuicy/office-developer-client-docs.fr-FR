---
title: Événements disponibles et leur DISPID (Outlook des API exportées)
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Décrit les identificateurs de répartition pour les événements Outlook disponibles.
ms.openlocfilehash: 7da8ad3d294699991584710b74bda375a708930e
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725512"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Événements disponibles et leur DISPID (Outlook des API exportées)

Cette section décrit les identificateurs de répartition pour les événements Outlook disponibles.
  
Outlook expose les identificateurs de distribution suivants (dispids) pour permettre aux modules de C++ d’écouter et de gérer les événements correspondants à partir de la fonction [IDispatch::Invoke](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke.md).
  
|**Constante**|**Dispid pour l’événement**|**Description**|**Paramètres**|**Remarques**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint**  |0xFC8E  |Permet de gérer l’événement au niveau de l’application à partir de la **fonction IDispatch::Invoke** qui se déclenche avant une opération d’impression. | Il existe 2 paramètres non nommés : le premier paramètre est de type VT_BOOL **\|VT_BREF**. **Renvoyer VARIANT_TRUE** dans ce paramètre pour annuler l’événement.  Le deuxième paramètre n’est pas utilisé et doit être ignoré. |Cette dispid est disponible depuis Outlook 2010. |
|**dispidEventReadComplete**  |0xFC8F  |Utilisé pour gérer l’événement au niveau de l’élément à partir de la fonction **IDispatch::Invoke** qui se déclenche lorsque Outlook a terminé la lecture des propriétés de l’élément. |Il n’existe qu’un seul _paramètre Cancel_ du type **VT_BOOL\| VT_BREF**. **Renvoyer VARIANT_TRUE** dans ce paramètre pour annuler l’opération de lecture. |Cette dispid est disponible depuis Outlook 2010. Cet événement correspond à l’événement Exchange Client Extensions (ECE) **IExchExtMessageEvents::OnReadComplete**, ainsi qu’à l’événement **ReadComplete** qui a été ajouté au modèle objet depuis Outlook 2013. |

Pour obtenir un exemple d’utilisation d’un dispid pour écouter et gérer un événement, `CAppEventListener::Invoke` voir la fonction dans la solution C++ Outlook décrite dans [Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Voir aussi

- [API exportées Outlook](outlook-exported-apis.md)
- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos des API exportées par Outlook](about-apis-exported-by-outlook.md)
- [Mise en Outlook des événements 2002/XP dans MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)
