---
title: Dossiers MAPI masqu�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
ms.openlocfilehash: 78ff715db51af9729cb9ec92595a638584b796f3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379870"
---
# <a name="mapi-hidden-folders"></a>Dossiers MAPI masqu�

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dossiers cach�s sont les dossiers g�n�riques clients cr�ent dans le dossier racine de la banque de messages, plut�t que dans le dossier racine d'une sous-arborescence message interpersonnel (IPM). �tant donn� que ces dossiers ne sont pas plac�s dans la sous-arborescence IPM, ils sont g�n�ralement masqu�s � partir de l'affichage de l'utilisateur par le fournisseur de banque de messages. Dossiers cach�s contient g�n�ralement des informations qui sont pertinentes pour la banque de messages, mais non pertinents pour l'utilisateur. Clients cr�er les dossiers cach�s pour stocker, par exemple, des informations suppl�mentaires � enregistrer avec le reste de la hi�rarchie de dossiers.
  
MAPI attend tous les clients puissent afficher, cr�er, modifier et supprimer des dossiers dans une sous-arborescence IPM. Prise en charge de l'utilisation de dossiers dans les autres arborescences est consid�r� comme facultatif. Toutefois, tous les magasins de message qui peut �tre utilis� en tant que la banque par d�faut et qui peut envoyer et recevoir des messages doivent prennent en charge les dossiers cach�s.
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

