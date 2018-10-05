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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382546"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un fournisseur de magasin de fichier (.pst) de dossiers personnels substituer la stratégie PSTDisableGrow.
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de banque PST  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Récupère la liste des enregistrements pour le fichier de dossiers personnels (.pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Enregistre les fichiers de dossiers personnels pour le déverrouillage automatique, en évitant les autres appels à HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Déverrouille le fichier de dossiers personnels de la croissance.  <br/> |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’Interface Gestionnaire remplacer PST pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous serez les trouver dans la rubrique [Constantes MAPI](mapi-constants.md) et peuvent copier et les ajouter à votre code. Pour associer les noms symboliques identificateur global unique (GUID) à leurs valeurs, utilisez la macro DEFINE_GUID définie dans le guiddef.h de fichier d’en-tête Kit de développement logiciel (SDK) de Microsoft Windows. 
  
Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

