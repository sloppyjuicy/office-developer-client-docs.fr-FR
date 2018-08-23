---
title: Utilisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569532"
---
# <a name="using-the-mapi-utilities"></a>Utilisation des utilitaires MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les utilitaires MAPI sont composés des données de la table et les objets de données de propriété et une variété de fonctions pour prendre en charge diverses fonctionnalités. Il est possible d’un client ont besoin seulement ces utilitaires et n’ont pas à se connecter au sous-système MAPI pour établir une connexion avec des fournisseurs de services. Si votre client appartient à cette catégorie, appelez la fonction API [ScInitMapiUtil](scinitmapiutil.md) au lieu de la fonction [exécuter MAPIInitialize](mapiinitialize.md) lors de l’initialisation. 
  
 **ScInitMapiUtil** permet aux clients d’utiliser des fonctions utilitaires qui requièrent allocateurs MAPI, mais qui ne demandent pas les allocateurs explicitement. Lorsqu’il est temps d’arrêter, appelez [DeinitMapiUtil](deinitmapiutil.md) pour libérer des ressources plutôt que [MAPIUninitialize](mapiuninitialize.md). Les clients qui appellent jamais **exécuter MAPIInitialize** ne doivent pas appeler **MAPIUninitialize**.
  
Si vous avez appelé **ScInitMapiUtil** plutôt que **d’exécuter MAPIInitialize** et utilisez des tables via les méthodes **ITableData** plutôt que par les méthodes **IMAPITable** , sachez que les notifications de table ne fonctionnent pas. Les notifications requièrent l’utilisation des bibliothèques de MAPI et [IMAPITable : IUnknown](imapitableiunknown.md).
  

