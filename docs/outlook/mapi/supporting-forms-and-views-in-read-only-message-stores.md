---
title: Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432428"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="6ca6e-103">Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ca6e-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="6ca6e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ca6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ca6e-p101">Si votre fournisseur de banque de messages autorise une autorisation en lecture seule dans le m�canisme de stockage sous-jacent, les applications clientes et le Gestionnaire de formulaire MAPI ne pourront pas effectuer certaines op�rations. En particulier, les clients ne pourront pas ajouter ou modifier des affichages personnalis�s et du Gestionnaire de formulaire MAPI ne pourront pas installer des formulaires dans les tableaux de contenu associ� � des dossiers de la banque.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-p101">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things. Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="6ca6e-p102">De nombreux magasins de message en lecture seule, qui est peut-�tre pas un probl�me. Si tel est le cas, le fournisseur de banque de messages est inutile prendre en charge les tables de contenu associ�e � tout. Toutefois, si votre fournisseur de banque de messages doit �tre en lecture seule et elle doit �galement prendre en charge un jeu pr�d�fini de vues ou de formulaires, qu'elle a besoin prendre en charge des tableaux de contenu associ�e.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-p102">For many read-only message stores, that may not be a problem. If that is the case, the message store provider does not need to support associated contents tables at all. However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="6ca6e-p103">La strat�gie la plus courante pour y parvenir, car les clients et le Gestionnaire de formulaire MAPI ne peut pas installer les affichages ou de stockent les formulaires dans le message elle-m�me, est pour le fournisseur de banque de messages pour coder les dans la banque de messages. Cela signifie que le contenu associ� ou des tables qui contiennent les affichages ou les formulaires devant exister dans la banque de messages lors de sa cr�ation, avant les clients ou de l'interface MAPI formulaire Gestionnaire jamais y acc�der. Puis, lorsque le client demande une table de contenu associ�e � obtenir des affichages personnalis�s � partir d'un formulaire ou le Gestionnaire de formulaire MAPI demande une table de contenu associ�e � un formulaire de lancement, le fournisseur de banque de message peut en fournir un.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-p103">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store. This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it. Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="6ca6e-p104">Cette exigence que les tables des mati�res associ�e cr��s et remplis lors de la cr�ation de la banque de messages proprement dit implique que votre fournisseur de banque de messages devront obtenir des informations sur le format des messages sp�ciaux que les clients et l'interface MAPI forment manager permet de stocker les formulaires et les affichages. Quels sont les formats varient selon le client et le Gestionnaire de formulaire MAPI est utilis�, afin que leur description ne peut pas �tre fournie ici.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-p104">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms. What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ca6e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ca6e-115">See also</span></span>



[<span data-ttu-id="6ca6e-116">Banques de messages en lecture seule</span><span class="sxs-lookup"><span data-stu-id="6ca6e-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

