---
title: Création d’applications MAPI sur les plateformes 32 bits et 64 bits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bc98b201b31048e22e093d92c9cf2d5ff1fb0257
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383148"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Création d’applications MAPI sur les plateformes 32 bits et 64 bits

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit les actions que les développeurs MAPI à suivre pour modifier et régénérer les applications MAPI 32 bits de s’exécuter sur une plateforme 64 bits et 64 bits des applications à exécuter sur une plateforme 32 bits. Dans cette rubrique, une plateforme 64 bits est un ordinateur équipé de 64 bits de Microsoft Outlook et Windows 64 bits, et une plateforme 32 bits est un ordinateur installé avec Outlook 32 bits de Windows 32 bits ou 64 bits. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Système d’exploitation et prise en charge Office pour Outlook 64 bits

> [!NOTE]
> Le nombre de bits à terme fait référence à la différence entre les architectures de processeur 32 bits et 64 bits et la compatibilité des applications associée. Dans cette rubrique, nombre de bits est utilisée pour indiquer la version de Windows, Microsoft Office, Outlook, ou une application MAPI conçue pour une architecture de processeur 32 bits ou 64 bits d’un ordinateur et éventuellement les autres applications qui s’exécutent sur cet ordinateur. 
  
À partir de Microsoft Office 2010, Outlook est disponible en tant qu’une édition 32 bits et une application 64 bits. Sur le même ordinateur, le nombre de bits d’Outlook varie selon le nombre de bits du système d’exploitation Windows (x86 ou x64) et de Microsoft Office, si Office est déjà installé sur cet ordinateur. Voici quelques-uns des facteurs qui déterminent la faisabilité de l’installation 32 bits ou une version 64 bits d’Outlook :
  
- Office 32 bits (et Outlook 32 bits) peuvent être installés sur une version 32 bits ou 64 bits du système d’exploitation Windows. Office 64 bits (Outlook 64 bits) peuvent uniquement être installés sur un système d’exploitation 64 bits.
    
-  L’installation par défaut d’Office sur une version 64 bits du système d’exploitation Windows est Office 32 bits.
    
- Le nombre de bits d’une version d’Outlook installée est toujours le même que le nombre de bits d’Office, si Office est installé sur le même ordinateur. En d’autres termes, une version 32 bits d’Outlook ne peut pas être installée sur le même ordinateur que celui qui a déjà les versions 64 bits d’autres applications Office, telles que 64 bits de Microsoft Word ou Microsoft Excel 64 bits. De même, une version 64 bits d’Outlook ne peut pas être installée sur le même ordinateur que celui qui a déjà les versions 32 bits d’autres applications Office.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Préparation d’applications MAPI pour les plateformes 32 bits et 64 bits

Les applications MAPI incluent des applications autonomes telles que Microsoft Communicator et MFCMAPI, fournisseurs de services de carnet d’adresses, stockent et fournisseurs de transport. Pour la fonction et la méthode MAPI appels fonctionnent dans une application MAPI (à l’exception d’une Simple fonction MAPI, MAPISendMail), le nombre de bits de l’application MAPI doivent être le même que le nombre de bits du sous-système MAPI sur l’ordinateur sur lequel l’application cible exécutez sur. Le nombre de bits du sous-système MAPI, est à son tour, déterminé par et toujours le même que le nombre de bits de la version installée d’Outlook. Le tableau suivant récapitule les actions nécessaires pour préparer les applications MAPI à exécuter sur les ordinateurs ciblés configurés avec Office et Windows du nombre de bits différents.
  
|Nombre de bits d’applications MAPI|Nombre de bits d’Outlook sur l’ordinateur cible|Nombre de bits de Windows sur l’ordinateur cible|Mesures nécessaires pour activer l’application s’exécute sur l’ordinateur cible|
|:-----|:-----|:-----|:-----|
|32 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Aucune action n’est nécessaire.  <br/> |
|32 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Reconstruire l’application sous la forme d’une application 64 bits. Dans le cas contraire, tous les appels méthode et fonction MAPI (à l’exception de **MAPISendMail**) échoue.  <br/> |
|64 bits  <br/> |64 bits  <br/> |64 bits  <br/> |Aucune action n’est nécessaire.  <br/> |
|64 bits  <br/> |32 bits  <br/> |32 bits ou 64 bits  <br/> |Reconstruire l’application sous la forme d’une application 32 bits. Dans le cas contraire, tous les appels méthode et fonction MAPI (à l’exception de **MAPISendMail**) échoue.  <br/> |
   
Plus les sections suivantes expliquent chaque scénario. Pour les scénarios qui nécessitent la recréation de l’application MAPI, voir [lien vers des fonctions MAPI](how-to-link-to-mapi-functions.md) pour plus d’informations sur la liaison à et appeler des fonctions MAPI. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>application de MAPI 32 bits et 32 bits Outlook

Les applications MAPI compilées pour un sous-système MAPI 32 bits qui est disponible dans les versions 32 bits d’Outlook, y compris les versions antérieures à Microsoft Outlook 2013, continuent à être pris en charge sur les ordinateurs installés avec Outlook 32 bits et une Windows 32 bits ou 64 bits Système d'exploitation. Aucune action n’est nécessaire pour les développeurs d’applications.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>application de MAPI 32 bits et 64 bits Outlook

les applications MAPI 32 bits ne sont pas pris en charge pour s’exécuter sur un ordinateur installé avec Outlook 64 bits et 64 bits de Windows. Le développeur d’applications doit mettre à jour et recréer l’application sous la forme d’une application 64 bits pour la plateforme 64 bits. Il s’agit comme une application 32 bits ne peut pas charger un fichier Msmapi32.dll de 64 bits. Il existe un petit nombre de modifications apportées aux API que les développeurs d’applications doivent comporter pour générer leur code avec succès pour un environnement 64 bits. Fichiers d’en-tête MAPI ont été mis à jour avec ces modifications pour prendre en charge de la plateforme 64 bits. Vous pouvez télécharger ces fichiers d’en-tête [Outlook 2010 : fichiers d’en-tête MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Développeurs peuvent utiliser ce même ensemble de fichiers d’en-tête MAPI pour créer des applications MAPI 32 bits et 64 bits.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>application de MAPI 64 bits et 64 bits Outlook

les applications MAPI 64 bits sont pris en charge sur les ordinateurs installés avec Outlook 64 bits et 64 bits de Windows. Aucune action n’est nécessaire pour les développeurs d’applications.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>application de MAPI 64 bits et 32 bits Outlook

les applications MAPI 64 bits ne sont pas pris en charge pour s’exécuter sur un ordinateur installé avec Outlook 32 bits et 32 bits ou 64 bits de Windows. Le développeur d’applications doit mettre à jour et recréer l’application sous la forme d’une application 32 bits fonctionne avec Outlook 32 bits. Utiliser les fichiers d’en-tête MAPI mis à jour, que vous pouvez télécharger à [Outlook 2010 : fichiers d’en-tête MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Développeurs peuvent utiliser ce même ensemble de fichiers d’en-tête MAPI pour créer des applications MAPI 32 bits et 64 bits.
  
### <a name="exception-mapisendmail"></a>Exception : MAPISendMail

En règle générale, une application de MAPI 32 bits doit s’exécute pas sur 64 bits plateforme (Outlook 64 bits sur Windows 64 bits) n’est pas premier reconstruit comme une application 64 bits et une application de MAPI 64-bit ne doivent pas exécuter sur un ordinateur installé avec Outlook 32 bits et 32 bits ou 64 bits Windows sans d’abord être recréés comme une application 32 bits. La figure 1 montre une boîte de dialogue qui s’affiche si une de ces scénarios se produit.
  
**La figure 1. Message d’erreur pour la plupart des cross-nombre de bits MAPI appelle.**

![Message d’erreur pour les appels MAPI plus nombre de cross-bits] (media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Message d’erreur pour les appels MAPI plus nombre de cross-bits")
  
Toutefois, un appel de fonction entre les éléments de tous les MAPI Simple et MAPI, **MAPISendMail**, doit réussir dans un scénario de Windows-64-bit-on-Windows-32-bit (WOW32) ou le Windows-32-bit-on-Windows-64-bit (WOW64) et n’entraîne pas de l’alerte ci-dessus. Ce scénario WOW64 s’applique uniquement à Windows 7. 

La figure 2 illustre un scénario WOW64 dans laquelle une application de MAPI 32 bits appelle **MAPISendMail** sur un ordinateur équipé de 64 bits de Windows 7. Dans ce scénario, la bibliothèque MAPI effectue un appel de COM pour lancer une application de Fixmapi 64 bits. L’application Fixmapi lie implicitement à la bibliothèque MAPI, qui achemine l’appel de fonction vers le stub MAPI Windows, qui à son tour transfère l’appel vers le stub MAPI Outlook, l’activation de l’appel de fonction **MAPISendMail** réussisse. 
  
**La figure 2. Traitement de MAPISendMail dans un scénario WOW64.**

![Traitement de MAPISendMail dans un scénario WOW64] (media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Traitement de MAPISendMail dans un scénario WOW64")
  
## <a name="see-also"></a>Voir aussi

- [Lien vers les fonctions MAPI](how-to-link-to-mapi-functions.md)

