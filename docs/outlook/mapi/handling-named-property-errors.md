---
title: Propriété nommée gestion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9ea1c4063c08844052618c50fe53fdc0064787a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783431"
---
# <a name="handling-named-property-errors"></a><span data-ttu-id="ea16a-103">Propriété nommée gestion</span><span class="sxs-lookup"><span data-stu-id="ea16a-103">Handling named property errors</span></span>
  
<span data-ttu-id="ea16a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea16a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea16a-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span><span class="sxs-lookup"><span data-stu-id="ea16a-p101">When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop.</span></span> 
  
<span data-ttu-id="ea16a-107">Lorsqu'un appel des r�sultats de r�ussite partielle, par exemple lorsque la demande est pour les noms qui correspondent aux identificateurs sp�cifiques et un ou plusieurs noms ne peut pas �tre trouv�, **GetNamesFromIDs** renvoie MAPI_W_ERRORS_RETURNED et place PT_ERROR dans le type de propri�t� pour la propri�t� manquante dans le tableau de balise de propri�t�.</span><span class="sxs-lookup"><span data-stu-id="ea16a-107">When a call results in partial success, such as when the request is for names that map to specific identifiers and one or more names cannot be found, **GetNamesFromIDs** returns MAPI_W_ERRORS_RETURNED and places PT_ERROR in the property type for the missing property in the property tag array.</span></span> 
  
<span data-ttu-id="ea16a-p102">Parfois un client effectue un appel � **GetNamesFromIDs** qui se traduit aucune propri�t� n'est retourn�e, tel que lorsqu'il n'y a aucuns propri�t�s dans un jeu de propri�t�s sp�cifi�, ou lorsque toutes les propri�t�s nomm�es sont de type exclu par le param�tre flags. Les clients peuvent tirer fournisseurs de services :</span><span class="sxs-lookup"><span data-stu-id="ea16a-p102">Sometimes a client makes a call to **GetNamesFromIDs** that results in no properties being returned, such as when there are no properties in a specified property set, or when all named properties are of a type excluded by the flags. Clients can expect service providers to:</span></span> 
  
- <span data-ttu-id="ea16a-110">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="ea16a-110">Return S_OK.</span></span>
    
- <span data-ttu-id="ea16a-111">D�finissez le contenu du pointeur de tableau de balise de propri�t� dans un tableau de balise de propri�t� nouvellement allou� avec son membre **cValues** d�fini sur z�ro.</span><span class="sxs-lookup"><span data-stu-id="ea16a-111">Set the contents of the property tag array pointer to a newly allocated property tag array with its **cValues** member set to zero.</span></span> 
    
- <span data-ttu-id="ea16a-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span><span class="sxs-lookup"><span data-stu-id="ea16a-112">Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL.</span></span> 
    
- <span data-ttu-id="ea16a-113">D�finir le contenu du nombre de structures **MAPINAMEID** � z�ro.</span><span class="sxs-lookup"><span data-stu-id="ea16a-113">Set the contents of the count of **MAPINAMEID** structures to zero.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ea16a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea16a-114">See also</span></span>

- [<span data-ttu-id="ea16a-115">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="ea16a-115">MAPI Named Properties</span></span>](mapi-named-properties.md)

