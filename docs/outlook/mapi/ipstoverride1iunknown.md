---
title: IPSTOVERRIDE1 IUnknown
description: IPSTOVERRIDE1 IUnknown permet à un fournisseur de magasin PST (Personal Folders File) de remplacer la stratégie PSTDisableGrow.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
ms.openlocfilehash: bfce2e91274415007d02495d1a72746cefb208ab
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448461"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un fournisseur de magasins PST (Personal Folders File) de remplacer la stratégie PSTDisableGrow.
  
|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  <br/> |Iunknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de magasin PST  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Récupère la liste des inscriptions pour le fichier Dossiers personnels (.pst). |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Inscrit les fichiers Dossiers personnels pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback. |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Déverrouille un fichier Dossiers personnels pour la croissance. |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’interface du gestionnaire de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable que vous avez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) , et vous pouvez les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier guiddef.h du fichier d’en-tête du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs. 
  
<!-- For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070). -->
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

