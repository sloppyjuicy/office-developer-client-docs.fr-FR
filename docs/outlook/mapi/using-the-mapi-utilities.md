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
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409985"
---
# <a name="using-the-mapi-utilities"></a>Utilisation des utilitaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les utilitaires MAPI sont constitués de données de table et d'objets de données de propriétés et de différentes fonctions pour prendre en charge diverses fonctionnalités. Il est possible pour un client de n'avoir besoin que de ces utilitaires et de ne pas avoir à se connecter au sous-système MAPI pour établir une connexion avec les fournisseurs de services. Si votre client est adapté à cette catégorie, appelez la fonction API [ScInitMapiUtil](scinitmapiutil.md) plutôt que la fonction [MAPIInitialize](mapiinitialize.md) lors de l'initialisation. 
  
 **ScInitMapiUtil** permet aux clients d'utiliser des fonctions utilitaires qui nécessitent des allocateurs MAPI, mais qui ne demandent pas les allocateurs de manière explicite. Au moment de l'arrêt, appelez [DeinitMapiUtil](deinitmapiutil.md) pour libérer des ressources plutôt que [MAPIUninitialize](mapiuninitialize.md). Les clients qui n'appellent jamais **MAPIInitialize** ne doivent pas appeler **MAPIUninitialize**.
  
Si vous avez appelé **ScInitMapiUtil** au lieu de **MAPIInitialize** et que vous utilisez des tables via les méthodes **ITableData** plutôt que par le biais des méthodes **IMAPITable** , sachez que les notifications de table ne fonctionneront pas. Les notifications requièrent l'utilisation des bibliothèques MAPI et la fonctionnalité [IMAPITable: IUnknown](imapitableiunknown.md).
  

