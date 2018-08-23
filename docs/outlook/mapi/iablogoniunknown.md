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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4421fcde6ccd2f2ac6245927d9d5d63ddc5200af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573515"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ressources accède à un fournisseur de carnet d’adresses.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposés par :  <br/> |Objets d’ouverture de session de carnet d’adresses  <br/> |
|Implémentée par :  <br/> |Fournisseurs de carnet d’adresses  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IABLogon  <br/> |
|Type de pointeur :  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur livre adresse précédente.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Lance le processus de fermeture de session.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Ouvre un conteneur, utilisateur ou les listes de distribution, de messagerie et retourne un pointeur vers une implémentation d’interface pour fournir un accès plus.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.  <br/> |
|[Conseiller](iablogon-advise.md) <br/> |Enregistre l’appelant pour recevoir des notifications d’événements spécifiques qui affectent un conteneur, utilisateur ou liste de distribution de messagerie.  <br/> |
|[L’avertissement](iablogon-unadvise.md) <br/> |Annule les notifications qui ont été précédemment configurées avec un appel à la méthode **Advise** .  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Ouvre une entrée du destinataire qui comporte des données qui résident dans un fournisseur de carnet d’adresses hôte.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Renvoie un tableau des modèles uniques pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir des informations générales sur les méthodes de l’interface **IABLogon** , voir [L’implémentation de connexion au fournisseur de Service](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

