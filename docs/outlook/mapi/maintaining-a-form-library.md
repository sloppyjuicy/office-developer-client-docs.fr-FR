---
title: Maintenance d'une bibliothèque de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408802"
---
# <a name="maintaining-a-form-library"></a>Maintenance d'une bibliothèque de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une bibliothèque de formulaires contient toutes les informations importantes relatives à un formulaire: ses propriétés, ses verbes et les fichiers exécutables de son serveur. Certains clients autorisent les utilisateurs à gérer, installer ou supprimer des serveurs de formulaires. Si vous souhaitez offrir cette fonctionnalité à vos utilisateurs, vous devez avoir accès à:
  
- Le fichier de configuration du serveur de formulaire, un fichier avec le. Extension CFG.
    
- Objet conteneur de la bibliothèque de formulaires, objet qui implémente l'interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) . 
    
Pour accéder au fichier de configuration ou à un chemin d'accès, utilisez des moyens quelconques. En règle générale, les clients présentent à l'utilisateur une boîte de dialogue permettant d'installer et de supprimer des serveurs de formulaires qui peuvent également être utilisés pour inviter l'utilisateur à indiquer l'emplacement du fichier de configuration.
  
Pour accéder au conteneur de la bibliothèque de formulaires, appelez la méthode [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) du gestionnaire de formulaires. TransMettez une valeur d'énumération pour spécifier la bibliothèque de formulaires à ouvrir et, si nécessaire, un pointeur vers l'objet que le gestionnaire de formulaires doit utiliser pour ouvrir la bibliothèque de formulaires. Par exemple, si vous ouvrez une [bibliothèque de formulaires de dossier](folder-form-libraries.md), transmettez un pointeur [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) . 
  
Une fois que **OpenFormContainer** a retourné le pointeur **IMAPIFormContainer** , appelez [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md), en fonction de la maintenance à effectuer. **InstallForm** ajoute un serveur de formulaire à la bibliothèque; **RemoveForm** supprime un serveur de formulaires de la bibliothèque. 
  

