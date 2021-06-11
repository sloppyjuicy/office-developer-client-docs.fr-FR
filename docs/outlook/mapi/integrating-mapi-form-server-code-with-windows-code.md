---
title: Intégration du code de serveur de formulaire MAPI à Windows code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332178"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Intégration du code de serveur de formulaire MAPI à Windows code

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Rappelez-vous que votre serveur de formulaires est une application Win32. Par conséquent, certaines tâches sont liées au chargement de votre serveur de formulaires en mémoire et à la sortie propre. Comme toutes Windows applications, le point d’entrée de votre serveur de formulaires est la **fonction WinMain.** Cette fonction est l’endroit approprié pour effectuer les tâches suivantes : 
  
- Création et inscription d’une classe de fenêtre afin que votre serveur de formulaires puisse interagir avec d’autres composants OLE.
    
- Création et inscription d’une ou de plusieurs classes de fenêtre pour les interfaces utilisateur de vos objets de formulaire.
    
- Appel de [la fonction MAPIInitialize.](mapiinitialize.md) **MAPIInitialize** gère également l’initialisation OLE requise pour vous. Cette action doit être effectuée une fois par instance de votre serveur de formulaires. 
    
- Inscription d’un atom global avec une représentation sous forme de chaîne de l’identificateur de classe (CLSID) du serveur de formulaires. Cet atom doit exister pendant toute la durée de vie du serveur de formulaires.
    
- Appel de la fonction OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) pour inscrire la fabrique de classes de votre serveur de formulaires auprès de OLE. 
    
- Création d’une fenêtre principale pour recevoir des messages. Cette fenêtre n’a probablement pas besoin d’être visible, car l’utilisateur interagira avec les fenêtres spécifiques associées à des objets de formulaire individuels. Toutefois, pendant le développement, la fenêtre principale peut être un emplacement pratique pour le débogage de la sortie ou du contrôle de votre serveur de formulaires.
    
- Création d’une boucle de message qui s’exécute pendant toute la durée de vie du serveur de formulaires, traduction et distribution des messages Windows vers des objets de formulaire actifs.
    
Lorsque votre serveur de formulaire se quitte, il doit effectuer les tâches suivantes :
  
- Appelez la fonction OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) pour révoquer l’inscription OLE de votre classe de message. 
    
- Appelez **MAPIUninitialize** pour fermer correctement la connexion du serveur de formulaires à MAPI. 
    
- Supprimez l’atom global qui contient la représentation de chaîne de l’identificateur de classe.
    
## <a name="see-also"></a>Voir aussi



[Écriture de code serveur de formulaires](writing-form-server-code.md)

