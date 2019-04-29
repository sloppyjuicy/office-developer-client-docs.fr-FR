---
title: Instances de disque et tables de cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436754"
---
# <a name="disk-instances-and-cache-tables"></a>Instances de disque et tables de cache

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour activer un formulaire, ses fichiers exécutables doivent être disponibles sur l'ordinateur de l'utilisateur. Si elles ne sont pas disponibles, elles doivent être copiées à partir de la bibliothèque de formulaires sur le disque local. Pour ce faire, le gestionnaire de formulaires par défaut crée un sous-répertoire dans le répertoire Windows de l'utilisateur afin qu'il contienne les fichiers exécutables du formulaire (. Exe,. HLPs). Ce répertoire est appelé instance de disque du formulaire.
  
Le gestionnaire de formulaires par défaut gère une table de toutes les instances de disque de sorte que si une instance de disque existe déjà, elle puisse être utilisée sans avoir à copier les fichiers de la bibliothèque de formulaires sur le disque de l'utilisateur. La table des instances de disque est gérée comme un cache le moins fréquemment utilisé. Si une nouvelle instance de disque est nécessaire, elle est copiée sur l'ordinateur de l'utilisateur, ce qui remplace l'instance de disque la moins fréquemment utilisée. La table de cache de l'instance de disque est ensuite mise à jour pour refléter la dernière configuration. La taille du cache disque est une option configurable par l'utilisateur, ce qui permet aux utilisateurs d'équilibrer la vitesse en fonction de la capacité de disque disponible.
  
En plus du cache d'instance de disque, le gestionnaire de formulaires par défaut gère une table d'instance en cours d'exécution qui répertorie toutes les instances en cours d'exécution des serveurs de formulaires sur l'ordinateur de l'utilisateur. Cela utilise la capacité de MAPI à maintenir les instances de formulaires inactives en cours d'exécution dans un État invisible jusqu'à ce qu'une forme de la classe de message de ce serveur de formulaire soit activée. En d'autres termes, les serveurs de formulaires peuvent être mis en cache dans la mémoire vive (RAM) pour réduire le nombre de fois qu'un formulaire exécutable doit se trouver dans une bibliothèque de formulaires et être chargé en mémoire à partir du disque ou sur le réseau. Comme le cache d'instance de disque, le cache d'instance en cours de fonctionnement se comporte de manière moins fréquemment utilisée afin qu'une instance de formulaire en cours d'exécution puisse être purgée du cache pour faire de la place à une autre instance de formulaire. Cette mise en cache est recherchée pour une instance en cours d'exécution d'un serveur de formulaires avant que les bibliothèques de formulaires soient recherchées pour le serveur de formulaires.
  
> [!NOTE]
> Le gestionnaire de formulaires par défaut affiche un indicateur de progression lors de l'installation d'un formulaire sur la station de travail d'un utilisateur, ce qui permet à l'utilisateur d'annuler l'opération. Ceci est particulièrement utile si la connexion de l'utilisateur au fichier exécutable du serveur de formulaires se trouve sur un réseau à faible bande passante. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

