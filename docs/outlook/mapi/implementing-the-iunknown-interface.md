---
title: Mise en œuvre de l’interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0d307b3bda9f5e4f6c4059589f4af23698cde9f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575637"
---
# <a name="implementing-the-iunknown-interface"></a>Mise en œuvre de l’interface IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les méthodes de l’interface [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) implémentées dans chaque objet MAPI, s’appliquent à la communication entre objets et à la gestion des objets. 
  
 **IUnknown** a trois méthodes : [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)et [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface permet** à un objet de déterminer si un autre objet prend en charge une interface particulière. Avec **QueryInterface**, deux objets sans connaissance préalable des fonctionnalités de l’un et de l’autre peuvent interagir. Si l’objet qui implémente **QueryInterface prend** en charge l’interface en question, il renvoie un pointeur vers l’implémentation de l’interface. Si l’objet ne prend pas en charge l’interface demandée, il renvoie la MAPI_E_INTERFACE_NOT_SUPPORTED valeur. 
  
Lorsque **QueryInterface renvoie** un pointeur d’interface demandé, il doit également augmenter le nombre de références du nouvel objet. Le nombre de références d’un objet est une valeur numérique utilisée pour gérer la durée de vie de l’objet. Lorsque le nombre de références est supérieur à 1, la mémoire de l’objet ne peut pas être libérée car elle est activement utilisée. Ce n’est que lorsque le nombre de références passe à 0 que l’objet peut être libéré en toute sécurité. 
  
Les deux autres **méthodes IUnknown,** **AddRef** et **Release,** gèrent le nombre de références. **AddRef** incrémente le nombre de références, tandis **que Release** le décrémente. Toutes les méthodes ou fonctions API qui retournent des pointeurs d’interface, telles que **QueryInterface,** doivent appeler **AddRef** pour incrémenter le nombre de références. Toutes les implémentations de méthodes qui reçoivent des pointeurs d’interface doivent appeler **Release** pour décrémenter le nombre lorsque le pointeur n’est plus nécessaire. **Les** libérations vérifient le nombre de références existantes, en libérant la mémoire associée à l’interface uniquement si le nombre est 0. 
  
> [!NOTE]
> Étant **donné qu’AddRef** et **Release** ne sont pas requis pour renvoyer des valeurs précises, les appelants de ces méthodes ne doivent pas utiliser les valeurs de retour pour déterminer si un objet est toujours valide ou a été détruit. 
  
## <a name="see-also"></a>Voir aussi



[Mise en œuvre des objets MAPI](implementing-mapi-objects.md)

