---
title: IPSTOVERRIDEREQ IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: df8a307588e93e108010912ee89e78e6a33fcb96
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770723"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d’un fournisseur de magasins de fichiers de dossiers personnels (PST).
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de magasin PST  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst). |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’interface du handler de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) et pourrez les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs. 
  
Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

