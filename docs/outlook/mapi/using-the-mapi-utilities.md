---
title: Utilisation des utilitaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
ms.openlocfilehash: aefb19e3a0c20d75623d30aca5090c574a151bf7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372737"
---
# <a name="using-the-mapi-utilities"></a>Utilisation des utilitaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les utilitaires MAPI sont composés d’objets de données de table et de données de propriétés, ainsi que de diverses fonctions pour prendre en charge diverses fonctionnalités. Il est possible pour un client de n’avoir besoin que de ces utilitaires et de ne pas avoir à se connecter au sous-système MAPI pour établir une connexion avec les fournisseurs de services. Si votre client s’inscrit dans cette catégorie, appelez la fonction API [ScInitMapiUtil](scinitmapiutil.md) plutôt que [la fonction MAPIInitialize](mapiinitialize.md) au moment de l’initialisation. 
  
 **ScInitMapiUtil** permet aux clients d’utiliser des fonctions utilitaires qui nécessitent des allocateurs MAPI, mais qui ne demandent pas explicitement les allocateurs. Au moment de l’arrêt, appelez [DeinitMapiUtil](deinitmapiutil.md) pour libérer des ressources plutôt que [MAPIUninitialize](mapiuninitialize.md). Les clients qui **n’appellent jamais MAPIInitialize** ne doivent pas appeler **MAPIUninitialize**.
  
Si vous avez appelé **ScInitMapiUtil** plutôt que **MAPIInitialize** et que vous utilisez des tables par le biais des méthodes **ITableData** plutôt que par le biais des méthodes **IMAPITable** , sachez que les notifications de tableau ne fonctionneront pas. Les notifications nécessitent l’utilisation des bibliothèques MAPI et [de IMAPITable : IUnknown](imapitableiunknown.md).
  

