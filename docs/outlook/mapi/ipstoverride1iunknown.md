---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315497"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un fournisseur de magasins de dossiers personnels (PST) de remplacer la stratégie PSTDisableGrow.
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de magasins PST  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Enregistre les fichiers de dossiers personnels pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Déverrouille un fichier dossiers personnels pour la croissance.  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’interface du handler de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) et pourrez les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs. 
  
Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

