---
title: IPSTOVERRIDEQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: Accède aux ressources d’un fournisseur de magasins PST (Personal Folders File).
ms.openlocfilehash: 19375742a545d5fbf6fa94b62bc831c197f90146
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448475"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d’un fournisseur de magasins PST (Personal Folders File).
  
|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  <br/> |Iunknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de magasin PST  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Lance la procédure de déverrouillage pour un fichier Dossiers personnels (.pst). |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’interface du gestionnaire de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable que vous avez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) , et vous pouvez les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier guiddef.h du fichier d’en-tête du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs. 
  
<!-- For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).
   -->
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

