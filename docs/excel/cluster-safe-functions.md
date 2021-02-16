---
title: Fonctions sécurisées de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409299"
---
# <a name="cluster-safe-functions"></a>Fonctions sécurisées de cluster

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Dans Excel 2013, Excel peut décharger les appels User-Defined Function (UDF) vers un cluster informatique hautes performances via une interface de connecteur de cluster dédiée. Les fournisseurs de clusters de calcul fournissent des connecteurs de cluster. Les auteurs UDF peuvent déclarer leurs UDF comme cluster-safe, puis, lorsqu’un connecteur de cluster est présent, Excel envoie des appels à ces UDF au connecteur de cluster pour le déchargement.
  
Lorsqu’Excel découvre une UDF sécurisée pour le cluster lors du recalcul, il transmet le nom de la XLL en cours d’exécution, le nom de l’UDF sécurisée pour le cluster et tous les paramètres au connecteur de cluster. Le connecteur exécute l’appel UDF à distance et renvoie les résultats à Excel. Les calculs non dépendants se poursuivent et lorsque le connecteur de cluster a terminé l’exécution de l’UDF, il transmet les résultats à Excel et les calculs dépendants se poursuivent. Le mécanisme de ce comportement asynchrone imite le mécanisme utilisé par les UDF asynchrones, sauf que le connecteur de cluster gère les aspects asynchrones au lieu de l’auteur UDF. En règle générale, un connecteur de cluster implémente un shim XLL pour charger des XLL et exécuter des UDF sur des nodes de cluster de calcul.
  
Les mécanismes de déclaration des UDF comme étant sécurisés pour les clusters ressemblent à ceux de la déclaration d’UDF comme étant sûrs pour le recalcul multi-thread. Toutefois, étant donné que l’UDF n’est pas nécessairement en cours d’exécution sur le même ordinateur que d’autres UDF de la même session Excel, il existe différentes considérations lors de l’écriture de UDF sécurisées pour le cluster.
  
Pour inscrire une UDF en tant que cluster-safe, vous devez appeler la fonction de rappel [xlfRegister (Formulaire 1)](xlfregister-form-1.md) via l’interface **Excel12** ou **Excel12v.** Pour plus d’informations sur ces interfaces, voir [Excel4/Excel12](excel4-excel12.md) et [Excel4v/Excel12v.](excel4v-excel12v.md) L’inscription d’une UDF en tant que cluster-safe via l’interface **Excel4** ou **Excel4v** n’est pas prise en charge. 
  
Si vous inscrivez une fonction en tant que cluster-safe, vous devez vous assurer que la fonction se comporte de manière sécurisée pour le cluster. Bien que le comportement exact du connecteur de cluster soit spécifique à l’implémentation, vous devez concevoir votre UDF de manière à ce qu’elle s’exécute sur un système informatique distribué et qu’elle présenterait les caractéristiques suivantes :
  
- Une UDF ne doit pas dépendre d’un état de mémoire. Par exemple, une UDF ne doit pas dépendre d’un cache en mémoire existant.
    
- Une UDF ne doit pas effectuer de rappels Excel que le fournisseur de connecteur de cluster ne prend pas en charge.
    
Outre le comportement sécurisé des clusters, il existe les restrictions techniques suivantes sur les UDF sécurisées pour les clusters :
  
1. Aucun argument XLOPER (types 'P', 'R').
    
2. Aucun argument XLOPER12 qui prise en charge les références de plage (type « U »).
    
3. Impossible d’être une fonction équivalente à une feuille macro (' # ' et &amp; ' ' cannot be combined).
    
Pour les UDF dont les durées d’exécution sont plus courtes, la surcharge du déchargement peut être supérieure au temps nécessaire à l’exécution de l’UDF, ce qui a pour effet de ne pas profiter de nombreux avantages de l’utilisation de cette infrastructure.
  
> [!NOTE]
> Vous ne pouvez pas déclarer une UDF sécurisée pour le cluster en tant que UDF asynchrone. 
  
Une UDF peut déterminer si elle est en cours d’utilisation à l’aide d’un connecteur de cluster en appelant la fonction de rappel [xlRunningOnCluster.](xlrunningoncluster.md) 
  

