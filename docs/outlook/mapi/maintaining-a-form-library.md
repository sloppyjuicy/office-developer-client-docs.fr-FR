---
title: Maintenance d’une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9d249456ff95affc8af8ff720e3f8ee72e48d072
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567265"
---
# <a name="maintaining-a-form-library"></a>Maintenance d’une bibliothèque de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une bibliothèque de formulaires contient toutes les informations importantes sur un formulaire : ses propriétés, ses verbes et les fichiers exécutables de son serveur. Certains clients permettent à leurs utilisateurs de gérer, d’installer ou de supprimer des serveurs de formulaires. Si vous souhaitez proposer cette fonctionnalité à vos utilisateurs, vous devez avoir accès à :
  
- Fichier de configuration du serveur de formulaire, un fichier avec le . Extension CFG.
    
- Objet conteneur de la bibliothèque de formulaires, objet qui implémente l’interface [IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md) 
    
Pour accéder au fichier de configuration ou à un chemin d’accès, utilisez n’importe quel moyen pratique. En règle générale, les clients présentent à l’utilisateur une boîte de dialogue pour installer et supprimer des serveurs de formulaires qui peuvent également être utilisés pour demander à l’utilisateur l’emplacement du fichier de configuration.
  
Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) du gestionnaire de formulaires. Passez une valeur d’éumération pour spécifier la bibliothèque de formulaires à ouvrir et, si nécessaire, un pointeur vers l’objet que le gestionnaire de formulaires doit utiliser pour ouvrir la bibliothèque de formulaires. Par exemple, si vous ouvrent une bibliothèque de formulaires de [dossiers,](folder-form-libraries.md)passez un pointeur [IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md) 
  
Après **qu’OpenFormContainer** renvoie le pointeur **IMAPIFormContainer,** appelez [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm,](imapiformcontainer-removeform.md)en fonction de la maintenance à effectuer. **InstallForm ajoute** un serveur de formulaire à la bibliothèque . **RemoveForm supprime** un serveur de formulaires de la bibliothèque. 
  

