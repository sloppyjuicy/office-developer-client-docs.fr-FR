---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417160"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie la table d'État en ajoutant une nouvelle ligne ou en modifiant une ligne existante.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cValues_
  
> dans Nombre de propriétés à inclure dans la ligne de tableau d'État nouvelle ou modifiée. 
    
 _lpColumnVals_
  
> dans Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à inclure en tant que colonnes dans la ligne de tableau d'État nouvelle ou modifiée.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les informations qui définissent la ligne de la table d'État sont traitées. L'indicateur suivant peut être défini:
    
STATUSROW_UPDATE 
  
> Indique à MAPI de fusionner les propriétés incluses dans le tableau vers lequel pointe _lpColumnVals_ avec une ligne de table d'État existante, et non dans une nouvelle ligne. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table d'État a été mise à jour avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: ModifyStatusRow** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **ModifyStatusRow** au moment de l'ouverture de session pour ajouter une ligne à la table d'État et à d'autres moments pendant la session pour mettre à jour la ligne. **ModifyStatusRow** fournit à MAPI les informations nécessaires pour créer la table d'État. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Définissez l'indicateur STATUSROW_UPDATE lorsque vous appelez **ModifyStatusRow** pour modifier les propriétés de votre ligne de table d'État existante. Cette opération informe MAPI que seules les colonnes modifiées sont transmises dans le paramètre _lpColumnVals_ . 
  
Les clients peuvent utiliser les informations de la table d'État pour accéder à votre objet d'État. 
  
Pour obtenir la liste complète des colonnes que vous devez inclure dans la ligne de votre tableau d'État, voir [Status tables](status-tables.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

