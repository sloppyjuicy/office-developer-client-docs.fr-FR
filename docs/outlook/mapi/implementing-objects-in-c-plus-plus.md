---
title: Implémentation des objets dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
ms.openlocfilehash: a5d9536ac519db6a7d7f0c11e1ffdaaa9d6e5b8c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371512"
---
# <a name="implementing-objects-in-c"></a>Implémentation des objets dans C++

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et fournisseurs de services C++ définissent des objets MAPI en créant des classes qui héritent des interfaces qu’ils implémentent. Chacune des méthodes d’interface est publique, tout comme le constructeur et le destructeur de la classe. Si la classe dispose de méthodes supplémentaires, elles peuvent être publiques ou privées, selon l’implémentation. Tous les membres de données sont privés. 
  
L’exemple de code suivant montre comment définir un objet d’état C++. La  `CMyMAPIObject` classe hérite de l’interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) . De nombreuses macros utilisées dans cet exemple sont définies dans le fichier d’en-tête OLE Compo ren.h. Les premiers membres de la classe sont les méthodes de l’interface de base, suivies des méthodes des interfaces héritées par ordre d’héritage. Les définitions d’interface suivantes sont les méthodes supplémentaires, le constructeur et le destructeur, ainsi que les membres de données. 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

Pour utiliser une instance de la  `CMyMAPIObject` classe, les clients ou fournisseurs de services C++ appellent l’une de ses méthodes comme suit : 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Voir aussi

- [Mise en œuvre des objets MAPI](implementing-mapi-objects.md)

