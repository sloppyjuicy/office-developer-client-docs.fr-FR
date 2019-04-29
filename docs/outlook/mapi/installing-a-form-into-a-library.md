---
title: Installation d'un formulaire dans une bibliothèque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433142"
---
# <a name="installing-a-form-into-a-library"></a>Installation d'un formulaire dans une bibliothèque

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le gestionnaire de formulaires MAPI par défaut fourni avec le kit de développement logiciel (SDK) Windows ne fournit pas d'interface utilisateur pour l'installation des formulaires dans les différentes bibliothèques de formulaires. Pour cette raison, vous devrez créer une petite application, ou un ensemble d'instructions détaillé, que les utilisateurs peuvent utiliser pour installer le formulaire.
  
Si vous implémentez une application d'installation, la série d'actions qu'elle doit effectuer pour installer un formulaire dans le tableau des contenus associés d'un dossier est la suivante:
  
1. Appelez la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) pour ouvrir le gestionnaire de formulaires. 
    
2. Utilisez [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) méthode pour sélectionner et ouvrir le conteneur cible pour le formulaire. 
    
3. Utilisez la fonction [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) pour installer le formulaire. 
    
    Les étapes 4 à 6 concernent l'installation dans une bibliothèque de formulaires locale:
    
4. Copiez tous les fichiers à l'emplacement approprié sur le disque local, si l'installation est effectuée vers la bibliothèque de formulaires locale sur la station de travail de l'utilisateur. Si nécessaire, modifiez le fichier de configuration du formulaire pour refléter les chemins d'accès actuels des composants. Le fichier de configuration de formulaire peut contenir des chemins d'accès relatifs, auquel cas cette étape n'est peut-être pas nécessaire.
    
5. Suivez les étapes d'enregistrement OLE appropriées pour associer le type de message au serveur de formulaires en cours d'installation.
    
6. Si le formulaire a été installé dans la bibliothèque de formulaires locale, copiez les fichiers icône (. ico) et de configuration (. cfg) du formulaire dans le répertoire%WINDOWS%\FORMS\CONFIGS afin que le formulaire puisse être restauré automatiquement si la bibliothèque de formulaires est endommagée ou supprimée. Cette étape est recommandée, mais pas obligatoire.
    
> [!NOTE]
> Vous pouvez simplifier l'installation dans une bibliothèque de formulaires locale en remplaçant les étapes 1 et 2 par un appel à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

