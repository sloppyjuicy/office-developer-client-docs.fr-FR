---
title: Intégration de code du serveur de formulaire MAPI avec du code Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397862"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Intégration de code du serveur de formulaire MAPI avec du code Windows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Rappelez-vous que votre serveur de formulaire est une application Win32. Par conséquent, il existe certaines tâches liées à charger votre serveur de formulaire en mémoire et en quittant l’application proprement. Comme toutes les applications Windows, le point d’entrée pour le serveur de votre formulaire est la fonction **WinMain** . Cette fonction est l’emplacement approprié pour effectuer les tâches suivantes : 
  
- Création et enregistrement d’une classe de fenêtre afin que votre serveur de formulaire peut interagir avec les autres composants OLE.
    
- Création et enregistrement d’une fenêtre ou les classes pour les interfaces utilisateur des objets de votre formulaire.
    
- L’appel de la fonction [exécuter MAPIInitialize](mapiinitialize.md) . **Exécuter MAPIInitialize** gère l’OLE initialisation requise, ainsi que. Il doit être effectuée une fois par instance de serveur de votre formulaire. 
    
- Inscription d’un atom globale avec une représentation de chaîne du serveur formulaire identificateurs de classe (CLSID). Cette atom doit exister pour la durée de vie du serveur du formulaire.
    
- L’appel de la fonction OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) pour inscrire la fabrique de classe de votre serveur de formulaire avec OLE. 
    
- Création d’une fenêtre principale pour recevoir des messages. Cette fenêtre n’a probablement pas besoin d’être visible, car l’utilisateur d’interagir avec les fenêtres spécifiques associées aux objets de formulaire individuel. Toutefois, lors du développement, la fenêtre principale peut être un emplacement pratique pour le débogage de sortie ou un contrôle de votre serveur de formulaire.
    
- Création d’une boucle de message qui s’exécute pendant la durée de vie du serveur de formulaire, traduction et répartir des messages windows aux objets du formulaire actif.
    
La fermeture de votre serveur de formulaire, il doit effectuer les tâches suivantes :
  
- Appelez la fonction OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) pour révoquer l’inscription de votre classe message OLE. 
    
- Appelez **MAPIUninitialize** pour fermer correctement la connexion du serveur formulaire MAPI. 
    
- Supprimer l’atom globale qui contient la représentation sous forme de chaîne de l’identificateur de classe.
    
## <a name="see-also"></a>Voir aussi



[Écriture de code du serveur de formulaire](writing-form-server-code.md)

