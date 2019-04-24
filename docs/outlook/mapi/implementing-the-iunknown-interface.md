---
title: Implémentation de l'interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310044"
---
# <a name="implementing-the-iunknown-interface"></a>Implémentation de l'interface IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les méthodes de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , implémentées dans chaque objet MAPI, prennent en charge la communication entre les objets et la gestion des objets. 
  
 **IUnknown** comporte trois méthodes: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)et [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permet à un objet de déterminer si un autre objet prend en charge une interface particulière. Avec **QueryInterface**, deux objets sans connaissance préalable de la fonctionnalité de chacun peuvent interagir. Si l'objet qui implémente **QueryInterface** prend en charge l'interface en question, il renvoie un pointeur vers l'implémentation de l'interface. Si l'objet ne prend pas en charge l'interface demandée, il renvoie la valeur MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
Lorsque **QueryInterface** renvoie un pointeur d'interface demandé, il doit également augmenter le nombre de références de l'objet. Le nombre de référence d'un objet est une valeur numérique utilisée pour gérer la durée de vie de l'objet. Lorsque le nombre de références est supérieur à 1, la mémoire de l'objet ne peut pas être libérée car elle est utilisée activement. C'est uniquement lorsque le nombre de références passe à 0, que l'objet peut être libéré en toute sécurité. 
  
Les deux autres méthodes **IUnknown** , **AddRef** et **Release**, gèrent le nombre de références. **AddRef** incrémente le décompte de références, tandis que **Release** le décrémente. Toutes les méthodes ou fonctions d'API qui renvoient des pointeurs d'interface, telles que **QueryInterface**, doivent appeler **AddRef** pour incrémenter le nombre de références. Toutes les implémentations de méthodes qui reçoivent des pointeurs d'interface doivent appeler **Release** pour décrémenter le nombre lorsque le pointeur n'est plus nécessaire. La **version** vérifie un décompte de références existant, libérant la mémoire associée à l'interface uniquement si le nombre est égal à 0. 
  
> [!NOTE]
> Comme **AddRef** et **Release** ne sont pas nécessaires pour renvoyer des valeurs exactes, les appelants de ces méthodes ne doivent pas utiliser les valeurs renvoyées pour déterminer si un objet est toujours valide ou a été détruit. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation d'objets MAPI](implementing-mapi-objects.md)

