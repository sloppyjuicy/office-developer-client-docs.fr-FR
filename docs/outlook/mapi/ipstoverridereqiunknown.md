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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356979"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d'un fournisseur de magasins de fichiers de dossiers personnels (PST).
  
|||
|:-----|:-----|
|Hérite de:  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de banque de fichiers PST  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Lance la procédure de déverrouillage pour un fichier de dossiers personnels (. pst).  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d'interface du gestionnaire des substitutions PST ne sont peut-être pas définis dans le fichier d'en-tête que vous avez actuellement, auquel cas vous les trouverez dans la rubrique [MAPI constants](mapi-constants.md) , et peuvent les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier d'en-tête Microsoft Windows Software Development Kit (SDK) guiddef. h pour associer les noms symboliques de GUID (identificateur global unique) et leurs valeurs. 
  
Pour plus d'informations, reportez-vous à la rubrique [implémentation d'un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

