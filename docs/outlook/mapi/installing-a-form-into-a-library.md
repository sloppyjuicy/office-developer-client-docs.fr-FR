---
title: Installation d’un formulaire dans une bibliothèque
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d3b20c9fb4b4f1a26eb4ed1a9a498bd56a915a70
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579780"
---
# <a name="installing-a-form-into-a-library"></a>Installation d’un formulaire dans une bibliothèque

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le Gestionnaire de formulaire MAPI par défaut fourni avec le Kit de développement Windows ne fournit pas une interface utilisateur pour l’installation de formulaires dans les différentes bibliothèques de formulaires. Pour cette raison, vous devez créer une petite application — ou détaillée du jeu d’instructions, que les utilisateurs peuvent utiliser pour installer le formulaire.
  
Si vous implémentez un programme d’installation, la série d’actions qu’il doit effectuer pour installer un formulaire dans le contenu associé d’un dossier tableau sont les suivants :
  
1. Appelez la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) pour ouvrir le formulaire gestionnaire. 
    
2. Utilisez [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour sélectionner et ouvrir le conteneur cible pour le formulaire. 
    
3. Utilisez la fonction [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) pour installer le formulaire. 
    
    Étapes 4 à 6 sont à l’installation dans une bibliothèque de formulaires local :
    
4. Copiez tous les fichiers vers l’emplacement approprié sur le disque local, si l’installation est à la bibliothèque de formulaires local sur le poste de travail. Si nécessaire, modifiez le fichier de configuration de formulaire pour refléter les chemins d’accès actuels des composants. Le fichier de configuration de formulaire peut contenir des chemins d’accès relatifs, auquel cas cette étape ne peut pas être nécessaire.
    
5. Effectuez les étapes de l’inscription OLE appropriées pour associer le type de message avec le serveur du formulaire en cours d’installation.
    
6. Si le formulaire a été installé dans la bibliothèque de formulaires local, copiez icône (.ico) et les fichiers de configuration (.cfg) du formulaire dans le répertoire %WINDOWS%\FORMS\CONFIGS afin que le formulaire peut être restauré automatiquement au cas où la bibliothèque de formulaires est endommagée ou supprimée. Cette étape est recommandée, mais pas obligatoire.
    
> [!NOTE]
> Vous pouvez simplifier l’installation à une bibliothèque de formulaires local en remplaçant les étapes 1 et 2 par un appel à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

