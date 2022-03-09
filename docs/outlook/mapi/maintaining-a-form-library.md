---
title: Maintenance d’une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
ms.openlocfilehash: b169565ec4463bf001e9f985e642b09b470a9ff3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371855"
---
# <a name="maintaining-a-form-library"></a>Maintenance d’une bibliothèque de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une bibliothèque de formulaires contient toutes les informations importantes sur un formulaire : ses propriétés, ses verbes et les fichiers exécutables de son serveur. Certains clients permettent à leurs utilisateurs de gérer, d’installer ou de supprimer des serveurs de formulaires. Si vous souhaitez proposer cette fonctionnalité à vos utilisateurs, vous devez avoir accès à :
  
- Fichier de configuration du serveur de formulaire, un fichier avec le . Extension CFG.
    
- Objet conteneur de la bibliothèque de formulaires, objet qui implémente l’interface [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) . 
    
Pour accéder au fichier de configuration ou à un chemin d’accès, utilisez n’importe quel moyen pratique. En règle générale, les clients présentent à l’utilisateur une boîte de dialogue pour installer et supprimer des serveurs de formulaires qui peuvent également être utilisés pour demander à l’utilisateur l’emplacement du fichier de configuration.
  
Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) du gestionnaire de formulaires. Passez une valeur d’éumération pour spécifier la bibliothèque de formulaires à ouvrir et, si nécessaire, un pointeur vers l’objet que le gestionnaire de formulaire doit utiliser pour ouvrir la bibliothèque de formulaires. Par exemple, si vous ouvrent une bibliothèque de [formulaires de dossiers](folder-form-libraries.md), passez un pointeur [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) . 
  
Une fois **qu’OpenFormContainer** renvoie le pointeur **IMAPIFormContainer** , appelez [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), en fonction de la maintenance à effectuer. **InstallForm ajoute** un serveur de formulaires à la bibliothèque . **RemoveForm supprime** un serveur de formulaires de la bibliothèque. 
  

