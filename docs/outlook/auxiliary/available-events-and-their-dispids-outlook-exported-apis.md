---
title: Événements disponibles et leurs DISPID (Outlook exportée API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Cette section décrit les identificateurs de répartition pour les événements Outlook rend disponible.
ms.openlocfilehash: 1542ff85579346a3674593e9ea38115170df2237
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782558"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Événements disponibles et leurs DISPID (Outlook exportée API)

Cette section décrit les identificateurs de répartition pour les événements Outlook rend disponible.
  
Outlook expose les identificateurs d’expédition suivants (DISPID) pour permettre aux compléments C++ écouter et gérer les événements à partir de la fonction [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) correspondants. 
  
|**Constante**|**DISPID, événement**|**Description**|**Paramètres**|**Remarques**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Utilisé pour gérer les événements de niveau application à partir de la fonction **IDispatch::Invoke** qui se déclenche avant une opération d’impression.  <br/> | Il existe des paramètres sans nom 2 :  <br/>  Le premier paramètre est de type ** VT_BOOL|VT_BREF **. Retourne la **valeur VARIANT_TRUE** dans ce paramètre pour annuler l’événement.  <br/>  Le deuxième paramètre n’est pas utilisé et doit être ignoré.  <br/> |Cette dispid est disponible depuis Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Permet de gérer l’événement au niveau élément à partir de la fonction **IDispatch::Invoke** qui se déclenche quand Outlook est terminée, les propriétés de l’élément de lecture.  <br/> |Il y n'a qu’un seul paramètre _Annuler_ qui est du type ** VT_BOOL|VT_BREF **. Retourne la **valeur VARIANT_TRUE** dans ce paramètre pour annuler l’opération de lecture.  <br/> |Cette dispid est disponible depuis Outlook 2010.  <br/> Cet événement correspond à l’événement d’Extensions de Client Exchange (ECE) **IExchExtMessageEvents::OnReadComplete**, et également à l’événement **ReadComplete** qui a été ajouté au modèle objet depuis Outlook 2013.  <br/> |
   
Pour obtenir un exemple d’utilisation d’un dispid pour écouter et gérer un événement, reportez-vous à la `CAppEventListener::Invoke` fonction dans la solution C++ Outlook décrite dans [L’implémentation Outlook 2002/XP récepteurs d’événements dans MFC C++ .NET 2003](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Voir aussi

- [Outlook des API exportées](outlook-exported-apis.md)
- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [À propos de l’API exporté par Outlook](about-apis-exported-by-outlook.md)
- [Récepteurs d’événements Outlook 2002/XP de mise en œuvre dans MFC C++ .NET 2003](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

