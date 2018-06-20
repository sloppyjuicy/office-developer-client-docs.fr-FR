---
title: Implémentation d’objets en langage C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784183"
---
# <a name="implementing-objects-in-c"></a>Implémentation d’objets en langage C++

**S’applique à**: Outlook 
  
Fournisseurs de services et les clients C++ définissent objets MAPI en créant des classes qui héritent des elles implémentent les interfaces. Chacune des méthodes de l’interface est public, le constructeur et le destructeur pour la classe. Si la classe dispose de méthodes supplémentaires, ils peuvent être publiques ou privées, en fonction de l’implémentation. Tous les membres de données sont privées. 
  
L’exemple de code suivant montre comment définir un objet d’état C++. Le `CMyMAPIObject` classe hérite de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. Bon nombre des macros utilisés dans cet exemple sont définies dans le fichier d’en-tête Compobj.h OLE. Les premiers membres de la classe sont les méthodes de l’interface de base, suivi par les méthodes des interfaces dans l’ordre de l’héritage des autorisations héritées. Les définitions d’interface sont d’autres méthodes, le constructeur et destructeur et les membres de données. 
  
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

Pour utiliser une instance de le `CMyMAPIObject` classe, clients C++ ou fournisseurs de services émettre un appel à l’une de ses méthodes, comme suit : 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Voir aussi

- [Implémentation d’objets MAPI](implementing-mapi-objects.md)

