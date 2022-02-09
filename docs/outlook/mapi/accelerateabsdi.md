---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ebc1c587ce663036f633971086fecccf0d0ff9d6
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461693"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel pour traiter les touches d’accès rapide dans une boîte de dialogue de carnet d’adresses sans mode. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction définie implémentée par :  <br/> |MAPI  <br/> |
|Fonction définie appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction. Dans les applications en cours d’exécution sur Microsoft Windows, _ulUIParam_ est le handle de fenêtre parent d’une boîte de dialogue et est de type HWND, cast en **ULONG_PTR**. La valeur zéro indique qu’il n’y a pas de fenêtre parente. 
    
 _lpvmsg_
  
> [in] Pointeur vers un Windows message.
    
## <a name="return-value"></a>Valeur renvoyée

Une fonction avec le prototype **ACCELERATEABSDI renvoie** true si elle gère le message. 
  
## <a name="remarks"></a>Remarques

Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue sans mode, c’est-à-dire, uniquement si l’application cliente a définie l’indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) . 
  
Une boîte de dialogue sans mode partage la boucle Windows message de l’application cliente, au lieu d’avoir sa propre boucle. L’application, qui contrôle la boucle de message, ne sait pas quelles touches d’accès rapide la boîte de dialogue utilise, elle appelle donc une fonction **ACCELERATEABSDI** pour tester et agir sur des touches d’accès rapide telles que Ctrl+P pour l’impression. 
  
La boucle de messages d’un client appelle la fonction **ACCELERATEABSDI** lorsque le client appelle une boîte de dialogue de carnet d’adresses sans mode avec la méthode [IAddrBook::Address](iaddrbook-address.md) . Cet appel est interrompu lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) . 
  

