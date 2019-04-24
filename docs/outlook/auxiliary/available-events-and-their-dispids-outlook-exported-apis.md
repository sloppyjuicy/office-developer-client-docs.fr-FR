---
title: Événements disponibles et leur DISPID (Outlook des API exportées)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Cette section décrit les identificateurs de dispatch pour les événements qu'Outlook met à disposition.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316876"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Événements disponibles et leur DISPID (Outlook des API exportées)

Cette section décrit les identificateurs de dispatch pour les événements qu'Outlook met à disposition.
  
Outlook expose les identificateurs de dispatch (DISPID) suivants pour permettre aux compléments C++ d'écouter et de gérer les événements correspondants à partir de la fonction [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) . 
  
|**Constante**|**DISPID pour l'événement**|**Description**|**Paramètres**|**Notes**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Permet de gérer l'événement au niveau de l'application à partir de la fonction **IDispatch:: Invoke** qui se déclenche avant une opération d'impression.  <br/> | Il y a 2 paramètres sans nom:  <br/>  Le premier paramètre est de type * * VT_BOOL|VT_BREF * *. Renvoyer **VARIANT_TRUE** dans ce paramètre pour annuler l'événement.  <br/>  Le deuxième paramètre n'est pas utilisé et doit être ignoré.  <br/> |Ce DISPID est disponible depuis Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Permet de gérer l'événement au niveau de l'élément à partir de la fonction **IDispatch:: Invoke** qui se déclenche quand Outlook a terminé de lire les propriétés de l'élément.  <br/> |Il n'y a qu'un seul paramètre _Cancel_ correspondant au type * * VT_BOOL|VT_BREF * *. Renvoyer **VARIANT_TRUE** dans ce paramètre pour annuler l'opération de lecture.  <br/> |Ce DISPID est disponible depuis Outlook 2010.  <br/> Cet événement correspond à l'événement des extensions client Exchange (ECE) **IExchExtMessageEvents:: OnReadComplete**, ainsi qu'à l'événement **ReadComplete** qui a été ajouté au modèle objet depuis Outlook 2013.  <br/> |
   
Pour obtenir un exemple d'utilisation d'un DISPID pour écouter et gérer un événement, reportez `CAppEventListener::Invoke` -vous à la fonction dans la solution Outlook pour C++ décrite dans la rubrique [Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .net](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Voir aussi

- [API exportées Outlook](outlook-exported-apis.md)
- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos des API exportées par Outlook](about-apis-exported-by-outlook.md)
- [Implémentation de récepteurs d'événements Outlook 2002/XP dans MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

