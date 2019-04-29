---
title: Gestion des erreurs des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429865"
---
# <a name="handling-named-property-errors"></a>Gestion des erreurs des propriétés nommées
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Lorsqu'un appel des r�sultats de r�ussite partielle, par exemple lorsque la demande est pour les noms qui correspondent aux identificateurs sp�cifiques et un ou plusieurs noms ne peut pas �tre trouv�, **GetNamesFromIDs** renvoie MAPI_W_ERRORS_RETURNED et place PT_ERROR dans le type de propri�t� pour la propri�t� manquante dans le tableau de balise de propri�t�. 
  
Parfois un client effectue un appel � **GetNamesFromIDs** qui se traduit aucune propri�t� n'est retourn�e, tel que lorsqu'il n'y a aucuns propri�t�s dans un jeu de propri�t�s sp�cifi�, ou lorsque toutes les propri�t�s nomm�es sont de type exclu par le param�tre flags. Les clients peuvent tirer fournisseurs de services : 
  
- Elles retournent S_OK.
    
- D�finissez le contenu du pointeur de tableau de balise de propri�t� dans un tableau de balise de propri�t� nouvellement allou� avec son membre **cValues** d�fini sur z�ro. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- D�finir le contenu du nombre de structures **MAPINAMEID** � z�ro. 
    
## <a name="see-also"></a>Voir aussi

- [MAPI des propri�t�s nomm�e](mapi-named-properties.md)

