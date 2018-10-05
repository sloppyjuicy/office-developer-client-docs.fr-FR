---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389105"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournisseur de magasin de ressources d’accès d’un fichier de dossiers personnels (PST).
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de banque PST  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’Interface Gestionnaire remplacer PST pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous serez les trouver dans la rubrique [Constantes MAPI](mapi-constants.md) et peuvent copier et les ajouter à votre code. Pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows. 
  
Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

