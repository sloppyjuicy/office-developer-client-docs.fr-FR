---
title: MAPIOpenLocalFormContainer
description: Décrit la fonction MAPIOpenLocalFormContainer et fournit la syntaxe, les paramètres, la valeur de retour, les remarques et la référence MFCMAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
ms.openlocfilehash: da823176b65a529e6bf240d2ffe7675e0740f5ed
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817045"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur d’interface vers la bibliothèque de formulaires locale. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _ppfcnt_
  
> [out] Pointeur vers un pointeur vers l’interface de bibliothèque de formulaires locale.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

L’interface vers laquelle un pointeur est retourné peut être utilisée par des programmes d’installation tiers pour installer des formulaires spécifiques à l’application dans la bibliothèque sans que le programme doive d’abord se connecter à MAPI. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnMAPIOpenLocalFormContainer  <br/> |MFCMAPI utilise la méthode **MAPIOpenLocalFormContainer** pour ouvrir le conteneur de formulaires local à afficher dans une nouvelle fenêtre. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

