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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c299af87976336656b7f52f6a24a43f59fc60710
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570134"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseur de magasin de ressources d’accès d’un fichier de dossiers personnels (PST).
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémentée par :  <br/> |Fournisseur de banque PST  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’Interface Gestionnaire remplacer PST pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous serez les trouver dans la rubrique [Constantes MAPI](mapi-constants.md) et peuvent copier et les ajouter à votre code. Pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows. 
  
Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

