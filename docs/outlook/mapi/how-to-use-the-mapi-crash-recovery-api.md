---
title: Utiliser l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 4287cd35670515f9e497f3e58df7f7952b0c2347
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376335"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Utiliser l’API de récupération sur incident MAPI

**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette rubrique contient un exemple de code en C++ qui montre comment appeler la fonction [MAPICrashRecovery](mapicrashrecovery.md) à partir de la fonction [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) . La [fonction MAPICrashRecovery](mapicrashrecovery.md) vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST).

Si la mémoire est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données sur le disque et empêche tout accès en lecture ou en écriture jusqu’à ce que le processus soit terminé. En vous assurant que les PST ou les systèmes d’exploitation sont dans un état cohérent avant l’issue du processus, vous pouvez empêcher Microsoft Outlook 2010 ou Microsoft Outlook 2013 d’afficher le message d’erreur suivant et d’éviter les problèmes de performances :
  
**Un fichier de données n’a pas été fermé correctement la dernière fois qu’il a été utilisé et a fait l’objet d’une vérification pour la recherche de problèmes. Les performances peuvent être affectées pendant la vérification.**
  
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

## <a name="see-also"></a>Voir aussi

- [À propos de l’API de récupération sur incident MAPI](about-the-mapi-crash-recovery-api.md)
- [MAPICrashRecovery](mapicrashrecovery.md)
