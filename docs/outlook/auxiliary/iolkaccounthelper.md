---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386410"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Fournit des fonctionnalités d’assistance dans la session MAPI en cours pour gérer les comptes.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[PlaceHolder1](iolkaccounthelper-placeholder1.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Obtient le nom du profil d’un compte.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Ouvre une session MAPI et conserve une référence à la session pour le Gestionnaire de comptes.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Libère l’objet de session MAPI qui a été renvoyée par [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est transmise à [IOlkAccountManager::Init](iolkaccountmanager-init.md) lors de l’initialisation du Gestionnaire de comptes. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

