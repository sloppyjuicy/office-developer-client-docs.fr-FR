---
title: ACCELERATEABSDI
description: ACCELERATEABSDI définit une fonction de rappel pour traiter les touches d’accélérateur dans une boîte de dialogue de carnet d’adresses sans mode.
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
ms.openlocfilehash: c98b6232066cf574374ff019c505a52667ec1c32
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771054"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI

**S’applique à** : Outlook 2013 | Outlook 2016
  
Définit une fonction de rappel pour traiter les touches d’accélérateur dans une boîte de dialogue de carnet d’adresses sans mode.
  
|Propriété |Valeur |
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
  
> [in] Valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction. Dans les applications s’exécutant sur Microsoft Windows, _ulUIParam_ est le handle de fenêtre parent pour une boîte de dialogue et est de type HWND, converti en **ULONG_PTR**. La valeur zéro indique qu’il n’y a pas de fenêtre parente.

 _lpvmsg_
  
> [in] Pointeur vers un message Windows.

## <a name="return-value"></a>Valeur renvoyée

Une fonction avec le prototype **ACCELERATEABSDI** retourne TRUE si elle gère le message.
  
## <a name="remarks"></a>Remarques

Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue sans mode, c’est-à-dire uniquement si l’application cliente a défini l’indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) .
  
Une boîte de dialogue sans mode partage la boucle de message Windows de l’application cliente, au lieu d’avoir sa propre boucle. L’application, qui contrôle la boucle de message, ne sait pas quelles touches d’accélérateur la boîte de dialogue utilise. Elle appelle donc une fonction basée sur **ACCELERATEABSDI** pour tester et agir sur des touches d’accélérateur telles que Ctrl+P pour l’impression.
  
La boucle de message d’un client appelle la fonction basée sur **ACCELERATEABSDI** lorsque le client appelle une boîte de dialogue carnet d’adresses sans mode avec la méthode [IAddrBook::Address](iaddrbook-address.md) . Cet appel se termine lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) .
  