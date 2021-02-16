---
title: Gestion des erreurs de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1dc676101d4c39544c9dd1fae94000db9963ea02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419078"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="36cbf-103">Gestion des erreurs de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="36cbf-103">Handling MAPI property errors</span></span>

<span data-ttu-id="36cbf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36cbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36cbf-105">Au lieu de panne compl�te ou r�ussite, les m�thodes **IMAPIProp** suivantes signale la r�ussite partielle :</span><span class="sxs-lookup"><span data-stu-id="36cbf-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="36cbf-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="36cbf-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="36cbf-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="36cbf-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="36cbf-108">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="36cbf-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="36cbf-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="36cbf-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="36cbf-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="36cbf-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="36cbf-p101">**GetProps** signale la r�ussite partielle lorsqu'il peut extraire au moins une des propri�t�s requises pour un objet. **GetProps** indique la r�ussite partielle en retournant l'avertissement MAPI_W_ERRORS_RETURNED et en pla�ant les informations sur les propri�t�s non disponibles dans le tableau de valeurs de propri�t� indiqu� par le param�tre **lppPropArray**. Entr�e d'une propri�t� non disponible dans ce tableau contient PT_ERROR pour le type de propri�t� dans le membre **ulPropTag** et MAPI_E_NOT_FOUND ou une autre valeur d'erreur appropri�s pour le membre **Value**. Par exemple, si un client appelle la m�thode de **GetProps** d'un dossier pour r�cup�rer les propri�t�s de trois et le troisi�me n'est pas disponible, le fournisseur de banque de messages place PT_ERROR dans le troisi�me type de propri�t� dans le tableau de valeurs de propri�t� et MAPI_E_NOT_FOUND dans la troisi�me valeur de la propri�t�.</span><span class="sxs-lookup"><span data-stu-id="36cbf-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="36cbf-p102">Les autres m�thodes **IMAPIProp** rapport R�ussite partielle diff�remment. Ces m�thodes rapport R�ussite partielle en retournant S_OK et en pla�ant les informations d'erreur dans une structure [SPropProblemArray](spropproblemarray.md) . Le tableau de valeurs de propri�t� dans **GetProps** qui contient les donn�es que si la m�thode a r�ussi ou �chou�, � la diff�rence du tableau de probl�me de propri�t� dans ces m�thodes existe uniquement s'il existe des erreurs et uniquement si l'appelant a inscrit int�r�t pour en savoir plus sur les erreurs. Les appelants doivent sp�cifier un pointeur valide **SPropProblemArray** pour enregistrer les informations d'erreur.</span><span class="sxs-lookup"><span data-stu-id="36cbf-p102">The other **IMAPIProp** methods report partial success differently. These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure. Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors. Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="36cbf-p103">Lorsqu'une valeur d'erreur est renvoy�e � partir de **SetProps**, **DeleteProps**, **CopyTo** ou **CopyProps**, cela indique �chec au lieu de r�ussite partielle. Le tableau de probl�me de propri�t�, le cas �ch�ant, n'est pas valide. Clients ne doivent pas essayer d'acc�der aux donn�es contenues dans la structure, ni qu'ils doivent essayer lib�rer la structure proprement dite. La r�ponse appropri�e consiste � appeler [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="36cbf-p103">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success. The property problem array, if available, is not valid. Clients should not try to access data held in the structure nor should they try to free the structure itself. The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="36cbf-p104">**GetLastError** est similaire � la fonction portant le m�me nom que celui fourni dans le SDK de Windows. Les deux fournissent que des informations d�taill�es sur une erreur qu'il n'est disponible avec la valeur de retour. Ils permettent tous deux renvoient des informations sur l'erreur pr�c�dente s'est produite. La diff�rence est que la fonction **GetLastError** Win32 les rapports d'erreur g�n�r�s par le thread d'appel et la m�thode **IMAPIProp::GetLastError** indique une erreur g�n�r�e par l'objet actuel. En d'autres termes, si un client appelle **DeleteProps** sur un message et le MAPI_E_NO_ACCESS est renvoy�e pour indiquer que le message est en lecture seule, **GetLastError** renvoie des donn�es fournies par le message.</span><span class="sxs-lookup"><span data-stu-id="36cbf-p104">**GetLastError** is similar to the function of the same name provided in the Windows SDK. Both provide more detailed information about an error than is available with the return value. They both return information about the previous error that has occurred. The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object. That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36cbf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36cbf-128">See also</span></span>

- [<span data-ttu-id="36cbf-129">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="36cbf-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

