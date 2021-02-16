---
title: IOlkAccountManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 544c87e5-887d-82ec-bf1a-0d95027fe0ec
ms.openlocfilehash: 5657aeb5f710281a1dcb482b3ebf15049e085b11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413653"
---
# <a name="iolkaccountmanager"></a>IOlkAccountManager

Gère l’accès aux comptes et définit les notifications concernant les modifications apportées aux comptes.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Fourni par :  <br/> |CLSID_OlkAccountManager  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkAccountManager  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Init](iolkaccountmanager-init.md) <br/> |Initialise le gestionnaire de comptes à utiliser.  <br/> |
|[DisplayAccountList](iolkaccountmanager-displayaccountlist.md) <br/> |Affiche la boîte de **dialogue Paramètres du compte** ou Ajouter un **nouveau** compte.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
|[FindAccount](iolkaccountmanager-findaccount.md) <br/> |Recherche un compte par valeur de propriété.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
|[DeleteAccount](iolkaccountmanager-deleteaccount.md) <br/> |Supprime le compte spécifié.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
|[SaveChanges](iolkaccountmanager-savechanges.md) <br/> |Enregistre les modifications apportées au compte spécifié.  <br/> |
|[GetOrder](iolkaccountmanager-getorder.md) <br/> |Obtient le classement de la catégorie de comptes spécifiée.  <br/> |
|[SetOrder](iolkaccountmanager-setorder.md) <br/> |Modifie l’ordre de la catégorie de comptes spécifiée.  <br/> |
|[EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |Obtient un éumérateur pour les comptes de la catégorie et du type spécifiques.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
|[FreeMemory](iolkaccountmanager-freememory.md) <br/> |Libère la mémoire allouée par **l’interface IOlkAccountManager.**  <br/> |
|[Conseiller](iolkaccountmanager-advise.md) <br/> |Enregistre un client auprès du gestionnaire de comptes pour les notifications concernant tous les comptes.  <br/> |
|[Unadvise](iolkaccountmanager-unadvise.md) <br/> |Désinsère un client auprès du gestionnaire de comptes pour les notifications pour tous les comptes.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté*  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

