---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348831"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d'un fournisseur de carnets d'adresses.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Exposé par:  <br/> |Objets d'ouverture de session du carnet d'adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d'adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IABLogon  <br/> |
|Type de pointeur:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](iablogon-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur du fournisseur de carnet d'adresses précédent.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Lance le processus de fermeture de session.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution, et renvoie un pointeur vers une implémentation d'interface pour fournir un accès supplémentaire.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.  <br/> |
|[Recommander](iablogon-advise.md) <br/> |Inscrit l'appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Annule les notifications précédemment configurées avec un appel à la **** méthode Advise.  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Ouvre l'objet d'État du fournisseur.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d'adresses hôte.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Renvoie une table des modèles uniques permettant de créer des destinataires à ajouter à la liste des destinataires d'un message sortant.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir des informations générales sur les méthodes de l'interface **IABLogon** , consultez la rubrique [Implementing Service Provider Logon](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

