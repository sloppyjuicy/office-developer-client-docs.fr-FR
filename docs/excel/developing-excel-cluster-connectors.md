---
title: Développement de connecteurs de cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412596"
---
# <a name="developing-excel-cluster-connectors"></a>Développement de connecteurs de cluster Excel

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Les connecteurs de cluster Excel permettent de décharger automatiquement les appels de fonctions définies par l'utilisateur en cluster dans un XLL sur un serveur en cluster. Pour obtenir une description des fonctions définies par l'utilisateur en cluster, consultez la rubrique [fonctions de sécurité du cluster](cluster-safe-functions.md). Ce délestage peut améliorer les performances en permettant l'utilisation de ressources de calcul supplémentaires. Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul à hautes performances.
  
## <a name="cluster-connectors"></a>Connecteurs de cluster

Un connecteur de cluster est une DLL qui fournit des points d'entrée définis utilisés par Excel pour coordonner les appels de fonctions définies par l'utilisateur en cluster. Il sert d'interface entre Excel et le cluster de calcul à hautes performances, pour la gestion des sessions, pour effectuer des appels de fonction (en transmettant le nom de la fonction Complete et les arguments réels de l'appel), et pour renvoyer les résultats de l'appel à Excel via un mécanisme de rappel.
  
Pour créer un connecteur de cluster, créez une DLL qui expose les points d'entrée figurant dans les [fonctions Excel cluster Connector](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Installation d'un connecteur de cluster

Pour qu'un connecteur de cluster soit disponible dans Excel, le code d'installation du connecteur doit installer la DLL du connecteur sur l'ordinateur sur lequel Excel est installé. En outre, le code d'installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante:
  
Connecteurs de cluster HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel \
  
Ajoutez un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes:
  
-  `Name`: nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.
    
-  `Filename`: chemin d'accès complet de la DLL.
    

