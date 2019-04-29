---
title: À propos de l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420261"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="07337-103">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="07337-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="07337-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07337-105">L'API de récupération d'urgence MAPI vérifie l'état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST) pour vérifier que les données sont dans un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="07337-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="07337-106">Si elle est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données des fichiers PST ou OSTs ouverts vers le disque et verrouille les fichiers PST ou OSTs et n'autorise pas l'accès aux données en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="07337-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="07337-107">Cela garantit que les données demeurent dans un état cohérent jusqu'à ce que le processus soit terminé.</span><span class="sxs-lookup"><span data-stu-id="07337-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="07337-108">En vous assurant que les fichiers PST ou OSTs sont dans un état cohérent avant la fin du processus, vous pouvez empêcher Microsoft Outlook 2013 et Microsoft Outlook 2010 d'afficher le message d'erreur suivant et éviter les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="07337-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="07337-109">**Un fichier de données ne s'est pas fermé correctement lors de sa dernière utilisation et est en cours de vérification des problèmes. Les performances peuvent être affectées lorsque la vérification est en cours.**</span><span class="sxs-lookup"><span data-stu-id="07337-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="07337-110">Cette API fournit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="07337-110">This API provides the following:</span></span>
  
<span data-ttu-id="07337-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="07337-111">Constants:</span></span>
  
- [<span data-ttu-id="07337-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="07337-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="07337-113">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="07337-113">Functions:</span></span>
  
- [<span data-ttu-id="07337-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="07337-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="07337-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07337-115">See also</span></span>



[<span data-ttu-id="07337-116">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="07337-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

