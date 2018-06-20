---
title: Méthode CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782021"
---
# <a name="closesession"></a><span data-ttu-id="a6325-103">Méthode CloseSession</span><span class="sxs-lookup"><span data-stu-id="a6325-103">CloseSession</span></span>

<span data-ttu-id="a6325-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6325-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a6325-105">Ferme une session avec un cluster.</span><span class="sxs-lookup"><span data-stu-id="a6325-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="a6325-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6325-106">Parameters</span></span>

<span data-ttu-id="a6325-107">_ID de session_</span><span class="sxs-lookup"><span data-stu-id="a6325-107">_SessionId_</span></span>
  
> <span data-ttu-id="a6325-108">ID de la session pour fermer.</span><span class="sxs-lookup"><span data-stu-id="a6325-108">The ID of the session to close.</span></span> <span data-ttu-id="a6325-109">Cette valeur doit correspondre à la valeur renvoyée par la [méthode OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="a6325-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6325-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a6325-110">Return value</span></span>

<span data-ttu-id="a6325-111">**xlHpcRetSuccess** si la session est fermée ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="a6325-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6325-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6325-112">See also</span></span>

- [<span data-ttu-id="a6325-113">Méthode OpenSession</span><span class="sxs-lookup"><span data-stu-id="a6325-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="a6325-114">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="a6325-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

