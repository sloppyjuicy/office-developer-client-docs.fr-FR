---
title: Fonctions sécurisées pour le cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782006"
---
# <a name="cluster-safe-functions"></a>Fonctions sécurisées pour le cluster

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Dans Excel 2013, Excel permettre transférer des appels de fonction définie par l’utilisateur (UDF) à un cluster de calcul hautes performances via une interface de connecteur de cluster dédié. Compute cluster fournissent connecteurs de Cluster. Auteurs UDF peuvent déclarer leur UDF en tant que cluster fiables, puis, lorsqu’un connecteur de cluster est présent, Excel envoyer les appels vers les UDF au connecteur de cluster pour le déchargement.
  
Lorsque Excel détecte un fichier UDF sécurisées pour le cluster pendant le recalcul, il passe le nom de la ressource XLL qui est en cours d’exécution, le nom de l’UDF sécurisées pour le cluster et tous les paramètres pour le connecteur de cluster. Le connecteur s’exécute à distance de l’appel des UDF et renvoie les résultats vers Excel. Calcul non dépendants continue et lorsque le connecteur de cluster a terminé l’UDF en cours d’exécution, il transmet les résultats vers Excel et calculs dépendants continuent. Le mécanisme de ce comportement asynchrone reproduit le mécanisme utilisé par les UDF asynchrones, sauf que le connecteur de cluster gère les aspects asynchrones au lieu de l’auteur UDF. En règle générale, un connecteur de cluster implémente un shim XLL pour charger les XLL et exécuter des UDF sur compute nœuds du cluster.
  
Les mécanismes de déclarer UDF sécurisées pour le cluster ressemblent à celles de la déclaration des UDF comme étant sécurisés pour le recalcul multi-thread. Toutefois, car l’UDF ne fonctionne pas nécessairement sur le même ordinateur que les autres fichiers UDF à partir de la même session Excel, il existe différentes Considérations lors de l’écriture de fonctions UDF sécurisées pour le cluster.
  
Pour enregistrer un fichier UDF comme sécurisées pour le cluster, vous devez appeler la fonction de rappel [xlfRegister (formulaire 1)](xlfregister-form-1.md) par le biais de l’interface **Excel12** ou **Excel12v** . Pour plus d’informations sur ces interfaces, voir le [Excel4/Excel12](excel4-excel12.md) et [Excel4v/Excel12v](excel4v-excel12v.md). Inscription d’un fichier UDF en tant que cluster sécurisé via l’interface **Excel4** ou **Excel4v** n’est pas pris en charge. 
  
Si vous enregistrez une fonction comme sécurisées pour le cluster, vous devez vous assurer que la fonction se comporte de façon sécurisées pour le cluster. Bien que le comportement exact du connecteur de cluster est spécifique à l’implémentation, vous devez concevoir votre UDF pour s’exécuter sur un système informatique distribué et ont les caractéristiques suivantes :
  
- Un fichier UDF doit s’appuie pas sur l’état de la mémoire. Par exemple, un fichier UDF doit s’appuie pas sur un cache en mémoire existant.
    
- Un fichier UDF ne doit pas effectuer des rappels Excel le fournisseur de connecteur de cluster ne prenant pas en charge.
    
Outre le comportement sécurisées pour le cluster, il existe les restrictions techniques suivantes sur les UDF sécurisées pour le cluster :
  
1. Aucun argument XLOPER (types « P », « R »).
    
2. Aucun argument XLOPER12 qui prennent en charge les références de plage (type « U »).
    
3. Ne peut pas être une fonction équivalente de feuille macro ('#' et '&amp;' ne peut être combinée).
    
Pour les UDF avec le temps d’exécution plus courts, la surcharge de déchargement peut être supérieure à la durée de l’UDF à exécuter, inversion de nombreux avantages de l’utilisation de cette infrastructure.
  
> [!NOTE]
> Vous ne pouvez pas déclarer un fichier UDF sécurisées pour le cluster en tant qu’une fichier UDF asynchrone. 
  
Un fichier UDF peut déterminer si elle est en cours d’exécution à l’aide d’un connecteur de cluster en appelant la fonction de rappel [xlRunningOnCluster](xlrunningoncluster.md) . 
  

