---
title: IABLogon IUnknown
description: Cet article décrit IABLogon IUnknown et fournit des méthodes, des propriétés et des remarques supplémentaires.
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
ms.openlocfilehash: cfcee38191fd18942e6219f467cbbd29c16ec725
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817269"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d’un fournisseur de carnet d’adresses.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets d’ouverture de session du carnet d’adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IABLogon  <br/> |
|Type de pointeur :  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member | Description |
|:-----|:-----|
|[Getlasterror](iablogon-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente du fournisseur de carnet d’adresses. |
|[Logoff](iablogon-logoff.md) <br/> |Lance le processus de fermeture de session. |
|[OpenEntry](iablogon-openentry.md) <br/> |Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution et retourne un pointeur vers une implémentation d’interface pour fournir un accès supplémentaire. |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[Conseiller](iablogon-advise.md) <br/> |Inscrit l’appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution. |
|[Non-surveillance](iablogon-unadvise.md) <br/> |Annule les notifications précédemment configurées avec un appel à la méthode **Advise** . |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur. |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Ouvre une entrée de destinataire qui contient des données résidant dans un fournisseur de carnet d’adresses hôte. |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Retourne une table de modèles uniques pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant. |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie. |
   
## <a name="remarks"></a>Remarques

Pour obtenir des informations générales sur les méthodes de l’interface **IABLogon** , consultez Implémentation de l’ouverture [de session du fournisseur de services](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

