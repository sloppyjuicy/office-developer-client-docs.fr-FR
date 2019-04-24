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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315497"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un fournisseur de magasins de fichiers de dossiers personnels (PST) de remplacer la stratégie PSTDisableGrow.
  
|||
|:-----|:-----|
|Hérite de:  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de banque de fichiers PST  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l'interface:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Récupère la liste des inscriptions pour le fichier de dossiers personnels (. pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Enregistre les fichiers de dossiers personnels pour le déverrouillage automatique, en évitant d'autres appels à HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Déverrouille un fichier de dossiers personnels pour la croissance.  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d'interface du gestionnaire des substitutions PST ne sont peut-être pas définis dans le fichier d'en-tête que vous avez actuellement, auquel cas vous les trouverez dans la rubrique [MAPI constants](mapi-constants.md) , et peuvent les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier d'en-tête Microsoft Windows Software Development Kit (SDK) guiddef. h pour associer les noms symboliques de GUID (identificateur global unique) et leurs valeurs. 
  
Pour plus d'informations, reportez-vous à la rubrique [implémentation d'un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

