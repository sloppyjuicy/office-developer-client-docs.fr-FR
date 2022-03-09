---
title: Installation d’un formulaire dans une bibliothèque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
ms.openlocfilehash: abcd4562f33cc38d552f89f12fca9da6db0fb857
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375194"
---
# <a name="installing-a-form-into-a-library"></a>Installation d’un formulaire dans une bibliothèque

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le gestionnaire de formulaire MAPI par défaut fourni avec le SDK Windows ne fournit pas d’interface utilisateur pour l’installation des formulaires dans les différentes bibliothèques de formulaires. Pour cette raison, vous devez créer une petite application ou un ensemble détaillé d’instructions que les utilisateurs peuvent utiliser pour installer le formulaire.
  
Si vous implémentez une application d’installation, la série d’actions qu’elle doit effectuer pour installer un formulaire dans la table des matières associée d’un dossier est la suivante :
  
1. Appelez la [fonction MAPIOpenFormMgr pour](mapiopenformmgr.md) ouvrir le gestionnaire de formulaires. 
    
2. Utilisez [la méthode IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour sélectionner et ouvrir le conteneur cible du formulaire. 
    
3. Utilisez la [fonction IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) pour installer le formulaire. 
    
    Les étapes 4 à 6 sont pour l’installation dans une bibliothèque de formulaires locale :
    
4. Copiez tous les fichiers à l’endroit approprié sur le disque local, si l’installation se fait dans la bibliothèque de formulaires locale sur la station de travail de l’utilisateur. Si nécessaire, modifiez le fichier de configuration du formulaire pour refléter les chemins d’accès actuels des composants. Le fichier de configuration du formulaire peut contenir des chemins d’accès relatifs, auquel cas cette étape n’est peut-être pas nécessaire.
    
5. Effectuer les étapes d’inscription OLE appropriées pour associer le type de message au serveur de formulaire en cours d’installation.
    
6. Si le formulaire a été installé dans la bibliothèque de formulaires locale, copiez les fichiers d’icône (.ico) et de configuration (.cfg) du formulaire dans le répertoire %WINDOWS%\FORMS\CONFIGS afin que le formulaire puisse être automatiquement restauré au cas où la bibliothèque de formulaires serait endommagée ou supprimée. Cette étape est recommandée, mais pas obligatoire.
    
> [!NOTE]
> Vous pouvez simplifier l’installation dans une bibliothèque de formulaires locale en remplaçant les étapes 1 et 2 par un appel à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

