---
title: Implémentation de l’interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f9ab3b75743d882aca0145b73b8ef707204cc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571898"
---
# <a name="implementing-the-iunknown-interface"></a>Implémentation de l’interface IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les méthodes de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , implémentée dans chaque objet MAPI, prend en charge la gestion de communication et l’objet inter-objet. 
  
 **IUnknown** a trois méthodes : [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)et [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permet à un objet déterminer si un autre objet prend en charge une interface particulière. Deux objets sans connaissance préalable de l’autre fonctionnalité peuvent interagir avec **QueryInterface**. Si l’objet qui implémente **QueryInterface** ne prend pas en charge l’interface en question, il retourne un pointeur vers l’implémentation de l’interface. Si l’objet ne prend pas en charge l’interface demandée, elle renvoie la valeur MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
**QueryInterface** retourne un pointeur d’interface demandé, il doit également augmenter le décompte de références du nouvel objet. Décompte de références d’un objet est une valeur numérique utilisée pour gérer la durée de vie de l’objet. Lorsque le décompte de références est supérieur à 1, ne peut pas libérer la mémoire de l’objet car il est utilisé activement. Il est uniquement lorsque le décompte de références atteint 0 que l’objet peut être libéré en toute sécurité. 
  
Les autres deux méthodes **IUnknown** , **AddRef** et **Release**, gérer le décompte de références. **AddRef** incrémente le décompte de références, lors de la **version** décrémente il. Toutes les méthodes ou des fonctions de l’API qui renvoient des pointeurs d’interface, tels que **QueryInterface**, doivent appeler **AddRef** pour incrémenter le décompte de références. Toutes les implémentations des méthodes qui reçoivent des pointeurs d’interface doivent appeler **Release** pour le décrémenter lorsque le pointeur n’est plus nécessaire. **Version** vérifie un décompte de références existantes, libérant ainsi la mémoire associée à l’interface uniquement si le nombre est 0. 
  
> [!NOTE]
> Parce que **AddRef** et **Release** ne sont pas nécessaires pour renvoyer des valeurs précises, les appelants de ces méthodes ne doivent pas utiliser les valeurs de retour pour déterminer si un objet est toujours valide ou a été détruit. 
  
## <a name="see-also"></a>Voir aussi



[Implémentation d’objets MAPI](implementing-mapi-objects.md)

