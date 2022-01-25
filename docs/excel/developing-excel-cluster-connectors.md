---
title: Développement Excel connecteurs de cluster
manager: lindalu
ms.date: 1/22/2022
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: Découvrez comment développer des connecteurs Excel cluster
ms.openlocfilehash: d6dbb7119f7a0fd849d4e26eb9d95b031f367976
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198435"
---
# <a name="developing-excel-cluster-connectors"></a>Développement de connecteurs de cluster Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Excel connecteurs de cluster fournissent un moyen de décharger automatiquement les appels de fonctions définies par l’utilisateur sécurisés du cluster dans un XLL vers un serveur en cluster. Pour obtenir une description des fonctions définies par l’utilisateur sécurisées pour le cluster, [voir Cluster Coffre Functions](cluster-safe-functions.md). Ce déchargement peut améliorer les performances en permettant d’utiliser davantage de ressources informatiques. Un connecteur de cluster est généralement développé par un fournisseur de cluster de calcul hautes performances.
  
## <a name="cluster-connectors"></a>Connecteurs de cluster

Un connecteur de cluster est une DLL qui fournit des points d’entrée définis qui Excel pour coordonner les appels de fonctions définies par l’utilisateur sécurisés du cluster. Il sert d’interface entre Excel et le cluster de calcul hautes performances, pour la gestion des sessions, pour effectuer des appels de fonction (en passant le nom complet de la fonction et les arguments réels de l’appel) et pour renvoyer les résultats des appels à Excel via un mécanisme de rappel.
  
Pour créer un connecteur de cluster, créez une DLL qui expose les points d’entrée répertoriés dans Excel fonctions du connecteur [de cluster.](excel-cluster-connector-functions.md)
  
## <a name="install-a-cluster-connector"></a>Installer un connecteur de cluster

Pour rendre un connecteur de cluster disponible dans Excel, le code d’installation du connecteur doit installer la DLL du connecteur sur l’ordinateur sur lequel Excel est installé. En outre, le code d’installation du connecteur doit ajouter une entrée pour le connecteur sous la clé de Registre suivante :
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Ajoutez un nœud à cette clé pour le connecteur de cluster qui spécifie les chaînes suivantes :
  
- `Name`—nom qui apparaîtra dans la liste des connecteurs de cluster dans Excel.

- `Filename`—chemin d’accès complet de la DLL.
