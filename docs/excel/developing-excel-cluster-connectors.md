---
title: Développement de connecteurs de Cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782009"
---
# <a name="developing-excel-cluster-connectors"></a>Développement de connecteurs de Cluster Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Connecteurs de cluster Excel fournissent un moyen de déchargement automatiquement les appels de fonction définie par l’utilisateur de sécurisées pour le cluster dans une solution XLL un serveur en cluster. Pour obtenir une description des fonctions définies par l’utilisateur de cluster sécurisé, voir [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md). Cette déchargement peut améliorer les performances en activant la plus de ressources informatiques à utiliser. Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul hautes performances.
  
## <a name="cluster-connectors"></a>Connecteurs de cluster

Un connecteur de cluster est une DLL qui fournit des points d’entrée définis que Microsoft Excel utilise pour coordonner les appels de fonction définie par l’utilisateur de sécurisées pour le cluster. Il sert d’interface entre Excel et le cluster de calcul hautes performances, pour la session de gestion, permettant de fonction appelle (en passant le nom complet de fonction et les arguments réels de l’appel) et pour retourner les résultats de l’appel vers Excel via un mécanisme de rappel.
  
Pour créer un connecteur de cluster, créez une DLL qui expose les points d’entrée répertoriés dans les [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Installation d’un connecteur de Cluster

Pour rendre un connecteur de cluster disponibles dans Excel, le code du programme d’installation du connecteur doit installer la DLL du connecteur sur l’ordinateur sur lequel Excel est installé. En outre, le code du programme d’installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante :
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Ajouter un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes :
  
-  `Name`— le nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.
    
-  `Filename`— le chemin d’accès complet de la DLL.
    

