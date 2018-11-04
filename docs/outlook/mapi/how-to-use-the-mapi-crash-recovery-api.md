---
title: Utiliser l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388503"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="f9501-103">Utiliser l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="f9501-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="f9501-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9501-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9501-105">Cette rubrique contient un exemple de code en langage C++ qui montre comment appeler la fonction [MAPICrashRecovery](mapicrashrecovery.md) à partir de la fonction [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9501-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="f9501-106">La fonction [MAPICrashRecovery](mapicrashrecovery.md) vérifie que l’état du fichier de dossiers personnels (PST) ou le fichier de dossiers en mode hors connexion (OST) de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="f9501-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="f9501-107">Si la mémoire est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données sur le disque et empêche plu accès en lecture ou écriture jusqu'à ce que le processus est terminé.</span><span class="sxs-lookup"><span data-stu-id="f9501-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="f9501-108">En s’assurant que les fichiers pst ou ost est dans un état cohérent avant que le processus est terminé, vous pouvez empêcher l’affichage du message d’erreur suivant Microsoft Outlook 2010 ou Microsoft Outlook 2013 et éviter les problèmes de performances :</span><span class="sxs-lookup"><span data-stu-id="f9501-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="f9501-109">**Un fichier de données ne pas fermer correctement la dernière fois qu’il a été utilisé et est en cours d’archivage pour les problèmes. Performances peuvent être affectées alors que la case à cocher est en cours.**</span><span class="sxs-lookup"><span data-stu-id="f9501-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="f9501-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9501-110">See also</span></span>

- [<span data-ttu-id="f9501-111">À propos de l’API de récupération sur incident MAPI</span><span class="sxs-lookup"><span data-stu-id="f9501-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="f9501-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f9501-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

