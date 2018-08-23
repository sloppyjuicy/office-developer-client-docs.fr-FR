---
title: Report des erreurs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3d2a46be04f235ba55aa5f2feef222ea7372b211
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569861"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="05d44-103">Report des erreurs MAPI</span><span class="sxs-lookup"><span data-stu-id="05d44-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="05d44-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05d44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05d44-p101">Quelques m�thodes d'interface acceptent l'indicateur MAPI_DEFERRED_ERRORS comme param�tre d'entr�e. Lorsque cet indicateur est d�fini, la m�thode n'a pas renvoy�e imm�diatement avec une valeur ; elle peut informer l'appelant le r�sultat de l'appel � un moment ult�rieur.</span><span class="sxs-lookup"><span data-stu-id="05d44-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="05d44-p102">Report d'erreurs permet de fournisseurs de services dans leur mise en �uvre des m�thodes complexes, rendant traitement plus rapidement. Plut�t que de g�rer les demandes de nombreuses et renvoi d'une valeur pour chacun, report d'erreurs autorise les appels � �tre fourni dans le fournisseur de services. Nombre de demandes de traitement � la fois permet de r�duire le trafic r�seau, ce qui am�liore les performances. Report des erreurs est particuli�rement utile dans les appels � supprimer ou de copier les propri�t�s, qui peuvent �tre tr�s longues op�rations.</span><span class="sxs-lookup"><span data-stu-id="05d44-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="05d44-p103">Lorsqu'un client effectue un appel sans la d�finition de l'indicateur MAPI_DEFERRED_ERRORS qui ne peut �tre trait�e que de mani�re diff�r�e, les fournisseurs de services peuvent diff�rer soit les erreurs, quel que soit ou renvoyer MAPI_E_TOO_COMPLEX. La plupart des clients doivent diff�rer des erreurs en tant qu'une strat�gie id�ale consisterait � l'�chec de l'appel.</span><span class="sxs-lookup"><span data-stu-id="05d44-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="05d44-p104">La d�finition de la MAPI_DEFERRED_ERRORS indicateur modifie gestion d'erreur d'un client mise en �uvre dans la mesure o� les informations renvoy�es peuvent �tre remises � tout moment, et non � un moment planifi�. Il est possible qu'une erreur � retourner lorsqu'il est trop tard pour faire quoi que ce soit � son sujet ou une fois que les donn�es relatives � la demande d'origine ne sont plus disponibles. Par exemple, si un client appelle **IMsgStore::OpenEntry** pour ouvrir un dossier supprim� avec MAPI_DEFERRED_ERRORS d�fini, le client ne sait pas du probl�me jusqu'� ce qu'un appel **IMAPIProp::GetProps** est effectu� pour r�cup�rer une des propri�t�s du dossier. **GetProps** retournera ensuite MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="05d44-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="05d44-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05d44-117">See also</span></span>



[<span data-ttu-id="05d44-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="05d44-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="05d44-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="05d44-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

