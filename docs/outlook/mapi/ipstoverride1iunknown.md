---
title: IPSTOVERRIDE1 IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 963749b9921a8e441c4655c238b58765b7e69d12
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774824"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à un fournisseur de magasins de fichiers de dossiers personnels (PST) de remplacer la stratégie PSTDisableGrow.
  
|||
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |Fournisseur de magasin PST  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst). |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Enregistre les fichiers dossiers personnels pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback. |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Déverrouille un fichier dossiers personnels pour la croissance. |
   
## <a name="remarks"></a>Remarques

Les identificateurs d’interface du handler de remplacement PST peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous les trouverez dans la rubrique [Constantes MAPI](mapi-constants.md) et pourrez les copier et les ajouter à votre code. Utilisez la macro DEFINE_GUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer des noms symboliques d’identificateur global unique (GUID) à leurs valeurs. 
  
Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

