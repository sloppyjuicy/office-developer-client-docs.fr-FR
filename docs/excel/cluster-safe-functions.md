---
title: Fonctions sécurisées en cluster
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
# <a name="cluster-safe-functions"></a>Fonctions sécurisées en cluster

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Dans Excel 2013, Excel peut décharger les appels UDF (fonction définie par l'utilisateur) vers un cluster informatique à hautes performances via une interface de connecteur de cluster dédiée. Les fournisseurs de cluster de calcul fournissent des connecteurs de cluster. Les auteurs de fichiers UDF peuvent déclarer les fichiers UDF comme étant sécurisés pour les clusters, puis, lorsqu'un connecteur de cluster est présent, Excel envoie des appels à ces UDF au connecteur de cluster pour le déchargement.
  
Lorsqu'Excel trouve une FDU de cluster sécurisée lors du recalcul, il transmet le nom de la XLL qui est en cours d'exécution, le nom de la FDU de cluster sécurisée et tous les paramètres du connecteur de cluster. Le connecteur exécute l'appel UDF à distance et renvoie les résultats à Excel. Le calcul non dépendant continue et lorsque le connecteur de cluster a terminé d'exécuter le fichier UDF, il transmet les résultats à Excel et les calculs dépendants continuent. Le mécanisme de ce comportement asynchrone imite le mécanisme utilisé par les fonctions définies par l'utilisateur asynchrone, à l'exception du fait que le connecteur de cluster gère les aspects asynchrones au lieu de l'auteur de la FDU. En règle générale, un connecteur de cluster implémente un shim XLL pour charger des XLL et exécuter des fonctions UDF sur les nœuds de cluster de calcul.
  
Les mécanismes de déclaration des FDU comme étant sécurisés pour les clusters ressemblent à ceux de la déclaration de FDU en toute sécurité pour le recalcul multi-thread. Toutefois, étant donné que la FDU n'est pas nécessairement exécutée sur le même ordinateur que d'autres UDF à partir de la même session Excel, il y a différentes considérations à prendre en compte lors de l'écriture de FDU de cluster.
  
Pour enregistrer une FDU comme étant sécurisée en clusters, vous devez appeler la fonction de rappel [xlfRegister (formulaire 1)](xlfregister-form-1.md) par le biais de l'interface **Excel12** ou **Excel12v** . Pour plus d'informations sur ces interfaces, voir [Excel4/Excel12](excel4-excel12.md) et [Excel4v/Excel12v](excel4v-excel12v.md). L'enregistrement d'une FDU en tant que sécurité de cluster via l'interface **Excel4** ou **Excel4v** n'est pas pris en charge. 
  
Si vous enregistrez une fonction de manière sécurisée en cluster, vous devez vous assurer que la fonction se comporte de façon sécurisée en cluster. Bien que le comportement exact du connecteur de cluster soit propre à l'implémentation, vous devez concevoir votre fichier UDF pour qu'il s'exécute sur un système informatique distribué et présenter les caractéristiques suivantes:
  
- Une FDU ne doit pas reposer sur un état de la mémoire. Par exemple, un fichier UDF ne doit pas reposer sur un cache en mémoire existant.
    
- Une FDU ne doit pas effectuer de rappels Excel que le fournisseur de connecteur cluster ne prend pas en charge.
    
Outre le comportement de cluster sécurisé, il existe les restrictions techniques suivantes sur les UDF de cluster:
  
1. Pas d'arguments XLOPER (types «P», «R»).
    
2. Aucun argument XLOPER12 prenant en charge les références de plage (tapez'U').
    
3. Ne peut pas être une fonction équivalente de feuille macro («&amp;#» et «» ne peuvent pas être combinées).
    
Pour les UDF avec des temps d'exécution plus courts, la charge de travail de déchargement peut être plus importante que le temps nécessaire à l'exécution du fichier UDF, ce qui annule la plupart des avantages de l'utilisation de cette infrastructure.
  
> [!NOTE]
> Vous ne pouvez pas déclarer une FDU de cluster sécurisée en tant que FDU asynchrone. 
  
Une FDU peut déterminer si elle est exécutée à l'aide d'un connecteur de cluster en appelant la fonction de rappel [xlRunningOnCluster](xlrunningoncluster.md) . 
  

