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
# <a name="deferring-mapi-errors"></a>Report des erreurs MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Quelques m�thodes d'interface acceptent l'indicateur MAPI_DEFERRED_ERRORS comme param�tre d'entr�e. Lorsque cet indicateur est d�fini, la m�thode n'a pas renvoy�e imm�diatement avec une valeur ; elle peut informer l'appelant le r�sultat de l'appel � un moment ult�rieur.
  
Report d'erreurs permet de fournisseurs de services dans leur mise en �uvre des m�thodes complexes, rendant traitement plus rapidement. Plut�t que de g�rer les demandes de nombreuses et renvoi d'une valeur pour chacun, report d'erreurs autorise les appels � �tre fourni dans le fournisseur de services. Nombre de demandes de traitement � la fois permet de r�duire le trafic r�seau, ce qui am�liore les performances. Report des erreurs est particuli�rement utile dans les appels � supprimer ou de copier les propri�t�s, qui peuvent �tre tr�s longues op�rations. 
  
Lorsqu'un client effectue un appel sans la d�finition de l'indicateur MAPI_DEFERRED_ERRORS qui ne peut �tre trait�e que de mani�re diff�r�e, les fournisseurs de services peuvent diff�rer soit les erreurs, quel que soit ou renvoyer MAPI_E_TOO_COMPLEX. La plupart des clients doivent diff�rer des erreurs en tant qu'une strat�gie id�ale consisterait � l'�chec de l'appel. 
  
La d�finition de la MAPI_DEFERRED_ERRORS indicateur modifie gestion d'erreur d'un client mise en �uvre dans la mesure o� les informations renvoy�es peuvent �tre remises � tout moment, et non � un moment planifi�. Il est possible qu'une erreur � retourner lorsqu'il est trop tard pour faire quoi que ce soit � son sujet ou une fois que les donn�es relatives � la demande d'origine ne sont plus disponibles. Par exemple, si un client appelle **IMsgStore::OpenEntry** pour ouvrir un dossier supprim� avec MAPI_DEFERRED_ERRORS d�fini, le client ne sait pas du probl�me jusqu'� ce qu'un appel **IMAPIProp::GetProps** est effectu� pour r�cup�rer une des propri�t�s du dossier. **GetProps** retournera ensuite MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Voir aussi



[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)

