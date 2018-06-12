---
title: Dossiers MAPI masqu�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 81b53bc138a64da673d6723e60fd90b086174efe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784627"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="d0cbc-103">Dossiers MAPI masqu�</span><span class="sxs-lookup"><span data-stu-id="d0cbc-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="d0cbc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0cbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0cbc-p101">Dossiers cach�s sont les dossiers g�n�riques clients cr�ent dans le dossier racine de la banque de messages, plut�t que dans le dossier racine d'une sous-arborescence message interpersonnel (IPM). �tant donn� que ces dossiers ne sont pas plac�s dans la sous-arborescence IPM, ils sont g�n�ralement masqu�s � partir de l'affichage de l'utilisateur par le fournisseur de banque de messages. Dossiers cach�s contient g�n�ralement des informations qui sont pertinentes pour la banque de messages, mais non pertinents pour l'utilisateur. Clients cr�er les dossiers cach�s pour stocker, par exemple, des informations suppl�mentaires � enregistrer avec le reste de la hi�rarchie de dossiers.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-p101">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree. Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider. Hidden folders typically contain information that is relevant to the message store but irrelevant to the user. Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="d0cbc-p102">MAPI attend tous les clients puissent afficher, cr�er, modifier et supprimer des dossiers dans une sous-arborescence IPM. Prise en charge de l'utilisation de dossiers dans les autres arborescences est consid�r� comme facultatif. Toutefois, tous les magasins de message qui peut �tre utilis� en tant que la banque par d�faut et qui peut envoyer et recevoir des messages doivent prennent en charge les dossiers cach�s.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-p102">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree. Support for working with folders in other trees is considered optional. However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0cbc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0cbc-112">See also</span></span>



[<span data-ttu-id="d0cbc-113">Dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="d0cbc-113">MAPI Folders</span></span>](mapi-folders.md)

