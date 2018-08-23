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
ms.openlocfilehash: 27b21162c53a64675abbf31a8ab512719b413d5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583161"
---
# <a name="disk-instances-and-cache-tables"></a>Instances de disque et tables de cache

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour activer un formulaire, ses fichiers exécutables doivent être disponibles sur l’ordinateur de l’utilisateur. Si elles ne sont pas disponibles, ils doivent être copiés à partir de la bibliothèque de formulaires sur le disque local. Pour ce faire, le Gestionnaire de formulaire par défaut crée un sous-répertoire dans le répertoire de l’utilisateur Windows pour contenir les fichiers exécutables du formulaire (. Exe. HLPs). Ce répertoire est appelé à l’instance du disque du formulaire.
  
Le Gestionnaire de formulaire par défaut gère un tableau de toutes les instances de disque afin que s’il existe déjà une instance de disque elle peut être utilisée sans avoir à copier les fichiers à partir de la bibliothèque de formulaires sur le disque de l’utilisateur. Le tableau des instances de disque est géré comme un cache moins fréquemment utilisés. Si une nouvelle instance de disque est nécessaire, il est copié dans l’ordinateur de l’utilisateur, en remplaçant l’instance de disque moins fréquemment utilisés. Le tableau de cache disque instance est alors mis à jour pour refléter la configuration le plus récent. La taille du cache disque est une option configurable par l’utilisateur, qui permet aux utilisateurs d’équilibrer la vitesse de la capacité disponible sur le disque.
  
Outre le cache disque de l’instance, le Gestionnaire de formulaire par défaut gère une table instance en cours d’exécution qui répertorie toutes les instances en cours d’exécution des serveurs de formulaire sur l’ordinateur de l’utilisateur. Possibilité de MAPI utilise pour conserver les instances du formulaire inactif en cours d’exécution dans un état invisible jusqu'à ce qu’un formulaire de ce message du serveur est activée de classe de formulaire. En d’autres termes, serveurs de formulaire peuvent être mis en cache dans la mémoire vive afin de réduire le nombre de fois exécutable d’un formulaire doit être situé dans une bibliothèque de formulaires et chargé en mémoire à partir du disque ou du réseau. Comme le cache disque de l’instance, le cache de l’instance en cours d’exécution se comporte de façon moins fréquemment utilisés afin qu’une instance de formulaire en cours d’exécution permettre être supprimée du cache pour libérer de l’espace pour une autre instance de formulaire. Ce cache est recherché dans une instance d’un serveur du formulaire en cours d’exécution avant des bibliothèques de formulaires sont recherchées pour le serveur du formulaire.
  
> [!NOTE]
> Le Gestionnaire de formulaire par défaut affiche un indicateur de progression lors de l’installation d’un formulaire sur une station de travail d’un utilisateur, l’activation de l’utilisateur à annuler l’opération. Ceci est particulièrement utile si la connexion de l’utilisateur à l’écran du fichier exécutable est sur un réseau de faible bande passante. 
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

