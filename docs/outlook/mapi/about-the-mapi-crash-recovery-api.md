---
title: À propos de l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576588"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="32df7-103">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="32df7-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="32df7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32df7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32df7-105">L’API de récupération de panne MAPI vérifie que l’état du fichier de dossiers personnels (PST) ou le fichier de dossiers en mode hors connexion (OST) de la mémoire pour vérifier que les données sont dans un état cohérent partagée.</span><span class="sxs-lookup"><span data-stu-id="32df7-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="32df7-106">Si elle est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données de l’ouvrir fichiers pst ou ost sur le disque et verrouille les fichiers pst ou ost et n’autorise pas l’accès en écriture aux données ni lecture.</span><span class="sxs-lookup"><span data-stu-id="32df7-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="32df7-107">Cela garantit que les données demeurent dans un état cohérent jusqu'à ce que le processus est terminé.</span><span class="sxs-lookup"><span data-stu-id="32df7-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="32df7-108">En s’assurant que les fichiers pst ou ost est dans un état cohérent avant que le processus est terminé, vous pouvez empêcher l’affichage du message d’erreur suivant Microsoft Outlook 2013 et Microsoft Outlook 2010 et éviter les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="32df7-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="32df7-109">**Un fichier de données ne pas fermer correctement la dernière fois qu’il a été utilisé et est en cours d’archivage pour les problèmes. Performances peuvent être affectées alors que la case à cocher est en cours.**</span><span class="sxs-lookup"><span data-stu-id="32df7-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="32df7-110">Cette API fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="32df7-110">This API provides the following:</span></span>
  
<span data-ttu-id="32df7-111">Constantes :</span><span class="sxs-lookup"><span data-stu-id="32df7-111">Constants:</span></span>
  
- [<span data-ttu-id="32df7-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="32df7-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="32df7-113">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="32df7-113">Functions:</span></span>
  
- [<span data-ttu-id="32df7-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="32df7-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="32df7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32df7-115">See also</span></span>



[<span data-ttu-id="32df7-116">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="32df7-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

