# Android Unsplash (Unofficial)
An unofficial Unsplash API library for Android

## Usage

### Get A List of Photos
~~~~~
Unsplash unsplash = new Unsplash(YOUR_CLIENT_ID);
unsplash.getPhotos(1, 10, Order.LATEST, new Unsplash.OnPhotosLoadedListener() {
    @Override
    public void onComplete(List<Photo> photos) {
        int photoCount = photos.size();
    }

    @Override
    public void onError(String error) {
        Log.v("Error", error);
    }
});
~~~~~

### Get A Photo By Id
~~~~~
Unsplash unsplash = new Unsplash(YOUR_CLIENT_ID);
unsplash.getPhoto(PHOTO_ID, new Unsplash.OnPhotoLoadedListener() {
    @Override
    public void onComplete(Photo photo) {
        String photoUrl = photo.getUrls().getRegular();
    }

    @Override
    public void onError(String error) {
        Log.v("Error", error);
    }
});
~~~~~

## To-Do
+ Statistics
+ Actions that require user authentication

# License
~~~
MIT License

Copyright (c) 2017 Keenen Charles

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

~~~
