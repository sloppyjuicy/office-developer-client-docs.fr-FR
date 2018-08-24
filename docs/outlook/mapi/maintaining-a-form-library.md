---
title: Maintenance d’une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6713055837e3b9b664d5fa1465c9a889919ee5ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590091"
---
# <a name="maintaining-a-form-library"></a>Maintenance d’une bibliothèque de formulaires

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une bibliothèque de formulaires conserve toutes les informations importantes sur un formulaire : ses propriétés, ses verbes et les fichiers exécutables de son serveur. Certains clients permettent à leurs utilisateurs à mettre à jour, installer ou supprimer des serveurs de formulaire. Si vous souhaitez offrir cette fonctionnalité à vos utilisateurs, vous devez avoir accès à :
  
- Fichier de configuration du serveur de formulaire, un fichier avec le. Extension CFG.
    
- Objet de conteneur de la bibliothèque de formulaires, un objet qui implémente le [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface. 
    
Pour accéder au fichier de configuration ou un chemin d’accès à celui-ci, utilisez procédé conviennent. En règle générale, les clients présenter l’utilisateur avec une boîte de dialogue pour l’installation et la suppression de serveurs de formulaire qui peuvent également être utilisées pour inviter l’utilisateur à l’emplacement du fichier de configuration.
  
Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode de [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) de responsable de l’écran. Transmettez une valeur d’énumération pour spécifier la bibliothèque formulaire à ouvrir et si nécessaire, un pointeur vers l’objet du Gestionnaire de formulaire à utiliser pour ouvrir la bibliothèque de formulaires. Par exemple, si vous ouvrez un [Dossier les bibliothèques de formulaires](folder-form-libraries.md), passez un [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointeur. 
  
Une fois que **OpenFormContainer** renvoie le pointeur **IMAPIFormContainer** , appelez [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), en fonction de la maintenance à effectuer. **InstallForm** ajoute un serveur de formulaire à la bibliothèque ; **RemoveForm** supprime un serveur de formulaire de la bibliothèque. 
  

