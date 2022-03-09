---
title: Afficher les dossiers MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
ms.openlocfilehash: 715ada62846ac59587d2ace770cf05acec69c44f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377721"
---
# <a name="mapi-view-folders"></a>Afficher les dossiers MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Afficher les dossiers sont les dossiers racine qui contiennent des informations associ�es pour d�finir des mises en page de l'autre affichage pour le contenu des dossiers de message interpersonnel (IPM). Afficher les dossiers se trouvent sous la racine de la banque de messages et, par cons�quent, ne sont pas visibles dans l'application cliente classique. Non � chaque banque de messages inclut les dossiers d'affichage ; Seuls les banques de messages qui sont configur�s pour fonctionner en tant que la banque de messages par d�faut pour la session doivent inclure les.  
  
MAPI prend en charge deux dossiers d'affichage :
  
- Communes � Le dossier d'affichage communs contient des vues qui sont standard pour la banque de messages et peuvent �tre utilis�s par n'importe quel utilisateur d'un client qui acc�de � la banque de messages. L’identificateur d’entrée du dossier d’affichage commun est stocké dans la propriété **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) de la boutique.
    
- Personnel � Le dossier d'affichage personnel contient des vues qui sont d�finies par un utilisateur particulier. MAPI définit la propriété **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) pour la gestion de l’identificateur d’entrée du dossier d’affichage personnel. � l'aide des affichages personnels, par exemple, un utilisateur peut se pr�senter � un groupe de messages tri�s par exp�diteur, r�pertoriant uniquement l'objet et l'accus� de r�ception date du message ; un autre utilisateur pourrait ressembler au m�me groupe tri� par date, r�pertoriant le sujet, l'exp�diteur et la taille de message.
    
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

