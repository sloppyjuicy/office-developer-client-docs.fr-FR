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
  
Pour activer un formulaire, ses fichiers exécutables doivent être disponibles sur l’ordinateur de l’utilisateur. S’ils ne sont pas disponibles, ils doivent être copiés à partir de la bibliothèque de formulaires sur le disque local. Pour ce faire, le gestionnaire de formulaires par défaut crée un sous-répertoire dans le répertoire Windows de l’utilisateur pour contenir les fichiers exécutables du formulaire (. EXE,. HLPs). Ce répertoire est appelé instance de disque du formulaire.
  
Le gestionnaire de formulaires par défaut tient à jour une table de toutes les instances de disque afin que, si une instance de disque existe déjà, elle puisse être utilisée sans avoir à copier des fichiers de la bibliothèque de formulaires sur le disque de l’utilisateur. La table des instances de disque est gérée en tant que cache le moins fréquemment utilisé. Si une nouvelle instance de disque est nécessaire, elle est copiée sur l’ordinateur de l’utilisateur, en remplaçant l’instance de disque la moins fréquemment utilisée. La table de cache des instances de disque est ensuite mise à jour pour refléter la configuration la plus récente. La taille du cache de disque est une option configurable par l’utilisateur, qui permet aux utilisateurs d’équilibrer la vitesse avec la capacité disque disponible.
  
Outre le cache d’instance de disque, le gestionnaire de formulaires par défaut tient à jour une table d’instances en cours d’exécution qui répertorie toutes les instances en cours d’exécution des serveurs de formulaires sur l’ordinateur de l’utilisateur. Cela utilise la capacité de MAPI à conserver les instances de formulaire inactives en cours d’exécution dans un état invisible jusqu’à ce qu’une forme de la classe de message de ce serveur de formulaires soit activée. En d’autres termes, les serveurs de formulaires peuvent être mis en cache en RAM pour réduire le nombre de fois que l’exécutable d’un formulaire doit être situé dans une bibliothèque de formulaires et chargé en mémoire à partir du disque ou sur le réseau. Comme le cache d’instance de disque, le cache d’instances en cours d’exécution se comporte de la manière la moins fréquemment utilisée afin qu’une instance de formulaire en cours d’exécution puisse être purgée du cache pour faire de la place à une autre instance de formulaire. Ce cache est recherché pour une instance en cours d’exécution d’un serveur de formulaires avant que les bibliothèques de formulaires ne soient recherchés pour le serveur de formulaires.
  
> [!NOTE]
> Le gestionnaire de formulaires par défaut affiche un indicateur de progression lors de l’installation d’un formulaire sur la station de travail d’un utilisateur, ce qui lui permet d’annuler l’opération. Ceci est particulièrement utile si la connexion de l’utilisateur au fichier exécutable du serveur de formulaire est sur un réseau à faible bande passante. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

