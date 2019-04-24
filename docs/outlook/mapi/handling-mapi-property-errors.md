---
title: Gestion des erreurs de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1dc676101d4c39544c9dd1fae94000db9963ea02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299386"
---
# <a name="handling-mapi-property-errors"></a>Gestion des erreurs de propriété MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Au lieu de panne compl�te ou r�ussite, les m�thodes **IMAPIProp** suivantes signale la r�ussite partielle : 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps** signale la r�ussite partielle lorsqu'il peut extraire au moins une des propri�t�s requises pour un objet. **GetProps** indique la r�ussite partielle en retournant l'avertissement MAPI_W_ERRORS_RETURNED et en pla�ant les informations sur les propri�t�s non disponibles dans le tableau de valeurs de propri�t� indiqu� par le param�tre **lppPropArray**. Entr�e d'une propri�t� non disponible dans ce tableau contient PT_ERROR pour le type de propri�t� dans le membre **ulPropTag** et MAPI_E_NOT_FOUND ou une autre valeur d'erreur appropri�s pour le membre **Value**. Par exemple, si un client appelle la m�thode de **GetProps** d'un dossier pour r�cup�rer les propri�t�s de trois et le troisi�me n'est pas disponible, le fournisseur de banque de messages place PT_ERROR dans le troisi�me type de propri�t� dans le tableau de valeurs de propri�t� et MAPI_E_NOT_FOUND dans la troisi�me valeur de la propri�t�. 
  
Les autres m�thodes **IMAPIProp** rapport R�ussite partielle diff�remment. Ces m�thodes rapport R�ussite partielle en retournant S_OK et en pla�ant les informations d'erreur dans une structure [SPropProblemArray](spropproblemarray.md) . Le tableau de valeurs de propri�t� dans **GetProps** qui contient les donn�es que si la m�thode a r�ussi ou �chou�, � la diff�rence du tableau de probl�me de propri�t� dans ces m�thodes existe uniquement s'il existe des erreurs et uniquement si l'appelant a inscrit int�r�t pour en savoir plus sur les erreurs. Les appelants doivent sp�cifier un pointeur valide **SPropProblemArray** pour enregistrer les informations d'erreur. 
  
Lorsqu'une valeur d'erreur est renvoy�e � partir de **SetProps**, **DeleteProps**, **CopyTo**ou **CopyProps**, cela indique �chec au lieu de r�ussite partielle. Le tableau de probl�me de propri�t�, le cas �ch�ant, n'est pas valide. Clients ne doivent pas essayer d'acc�der aux donn�es contenues dans la structure, ni qu'ils doivent essayer lib�rer la structure proprement dite. La r�ponse appropri�e consiste � appeler [IMAPIProp::GetLastError](imapiprop-getlasterror.md). 
  
**GetLastError** est similaire � la fonction portant le m�me nom que celui fourni dans le SDK de Windows. Les deux fournissent que des informations d�taill�es sur une erreur qu'il n'est disponible avec la valeur de retour. Ils permettent tous deux renvoient des informations sur l'erreur pr�c�dente s'est produite. La diff�rence est que la fonction **GetLastError** Win32 les rapports d'erreur g�n�r�s par le thread d'appel et la m�thode **IMAPIProp::GetLastError** indique une erreur g�n�r�e par l'objet actuel. En d'autres termes, si un client appelle **DeleteProps** sur un message et le MAPI_E_NO_ACCESS est renvoy�e pour indiquer que le message est en lecture seule, **GetLastError** renvoie des donn�es fournies par le message. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

