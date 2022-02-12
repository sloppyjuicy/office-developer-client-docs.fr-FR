---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a4e383b727f36b020bb0b8b72323d35f0ce8c240
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780035"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources dans un fournisseur de carnet d’adresses.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets d’logo de carnet d’adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IABLogon  <br/> |
|Type de pointeur :  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur de carnet d’adresses précédente. |
|[Logoff](iablogon-logoff.md) <br/> |Lance le processus de ffage de logo. |
|[OpenEntry](iablogon-openentry.md) <br/> |Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution et renvoie un pointeur vers une implémentation d’interface pour fournir un accès supplémentaire. |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[Conseiller](iablogon-advise.md) <br/> |Inscrit l’appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution. |
|[Unadvise](iablogon-unadvise.md) <br/> |Annule les notifications précédemment définies avec un appel à la **méthode Advise** . |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur. |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d’adresses hôte. |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Renvoie une table de modèles unique pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant. |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie. |
   
## <a name="remarks"></a>Remarques

Pour obtenir des informations générales sur les méthodes de l’interface **IABLogon** , voir [Implementing Service Provider Logon](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

