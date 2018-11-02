---
title: Prise en charge de plusieurs clients l'acc�s aux Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b13fbb9f2807c9814fed5ba3bcca8fe73aaa7b01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564219"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="57770-103">Prise en charge de plusieurs clients l'acc�s aux Messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="57770-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="57770-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57770-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57770-p101">Il est possible pour plusieurs applications clientes ouvrir un message donn� simultan�ment. Fournisseurs de banque de messages n'ont pas � suivre toutes les r�gles de gouvernance de ce type d'acc�s particuliers. Toutefois, si les applications clientes modifier le message et enregistrement leurs modifications, le fournisseur de magasins doit respecter les avec les r�gles suivantes :</span><span class="sxs-lookup"><span data-stu-id="57770-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="57770-108">Autoriser le premier appel � la m�thode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) afin de passer comme s'il �tait le seul client o� le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="57770-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="57770-109">Dans les appels suivants **SaveChanges** par d'autres clients, le fournisseur de banque de messages doit ignorer les modifications et retourner MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="57770-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="57770-p102">Permettent aux applications clientes r�pondre � un code de retour MAPI_E_OBJECT_CHANGED en appelant **SaveChanges** � l'aide de l'indicateur FORCE_SAVE. Si une application cliente effectue cette action, le fournisseur de banque de messages doit remplacer les modifications pr�c�dentes avec les nouveaux.</span><span class="sxs-lookup"><span data-stu-id="57770-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="57770-112">Sinon, le fournisseur de banque de messages peut d�tecter le conflit et pr�sentent une interface qui permet � l'utilisateur de choisir s'il faut conserver le message d'origine, remplacer le message d'origine avec les nouvelles modifications ou enregistrer les modifications apport�es � un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="57770-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57770-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57770-113">See also</span></span>



[<span data-ttu-id="57770-114">Implémentation des messages dans les banques de messages</span><span class="sxs-lookup"><span data-stu-id="57770-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

